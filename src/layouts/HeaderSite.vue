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
              class="q-py-xs q-pl-xl col-4"
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
                <q-icon name="my_location" 
                  color="green"   
                  class="cursor-pointer" 
                  />
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
export default {
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
<style>
.q-placeholder {
   text-align: left;

} 
</style>