<template>
    <q-header class="bg-white">
        <q-toolbar class="q-ma-lg" style="padding-left:35px;"> 
            <img src="~assets/logo.png"/>
             
            <!-- location Search --> 
            <q-input 
              outlined 
              bottom-slots 
              v-model="text" 
              placeholder="Type Your Location"  
              dense
              class="q-py-xs q-pl-xl"
              style="width:28%"
              @focus="MapSearch" 
              @blur="MapSearch"
            > 
              <template v-slot:prepend v-if="isVisible">
                <q-icon 
                  name="place"
                  color="red"
                />
              </template> 
              <template v-slot:append v-if="isVisible"> 
                  <Popper arrow placement="bottom-end" class="my-Oxygen" >
                       <q-icon name="my_location" 
                        color="green"   
                        class="cursor-pointer" 
                        />
                        <template #content> 
                            We couldn't find you on the map. 
                            Please allow us to access your location. 
                        </template>
                  </Popper>  
              </template>  
            </q-input>
            <q-space />  
            <div style="margin-right:80px;">
              <q-btn 
                outline
                style="color:#E4E8E7"  
                icon="local_mall"
                class="q-mx-sm"
              />
              <q-btn 
                outline
                style="color:#E4E8E7"   
                no-caps
              >
                <span class="text-grey-7">Login/Sign Up</span>
              </q-btn>
            </div>

        </q-toolbar>
      </q-header>
</template>
<script>
import Popper from "vue3-popper";
export default {
    components:{Popper},
    data(){
      return{
        isVisible : false
      }
    },
    methods:{
      MapSearch(){
          this.isVisible = !this.isVisible 
      }
    }
}
</script> 

<style scoped>
.q-placeholder {
   text-align: left;

}
:deep(.popper) {
    background: #FCDFDB;
    padding: 15px;
    border-radius: 10px;
    color: #000;
    font-size: 14px;
    width: 350px;
    left:130px;
    box-shadow: 0px 10px 15px 4px rgba(0,0,0,0.1);
    font-weight: bold;
  }

  :deep(.popper #arrow::before) {
    background: #FCDFDB;
    left:-5px;
  }

  :deep(.popper:hover),
  :deep(.popper:hover > #arrow::before) {
    background: #FCDFDB;
  }
</style>