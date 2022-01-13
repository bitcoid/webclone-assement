<template>
    <div class="row my-Oxygen" style="margin-left:-10px;">
          <div class="col-4 q-pa-sm" v-for="n in 5" :key="n">
              <q-card 
                  v-ripple class="my-box cursor-pointer q-hoverable"
                  flat
              >
                  <q-card-section horizontal>
                      <q-card-section>
                        <q-img
                            class="rounded-borders"
                            src="~assets/4a4aac07_5e40df724ba.jpeg"
                            style="width:120px"
                        />
                      </q-card-section>
                      <q-card-section> 
                        <div class="text-subtitle1 q-mt-sm q-mb-xs text-left">
                          Seo Goo Lalapan Ikan Laut Bakar/Goreng (Banyak Pilihan Ikan)
                        </div>
                        <div class="text-caption text-grey  text-left">
                            Goreng Krispi Campur Gurita, Udang, & Cumi (Octopus, ..)
                        </div>
                        <div class="text-right">
                            <Popper arrow placement="bottom-end" class="my-Oxygen" >
                                <q-btn color="green" class="text-white" icon="add" dense/>
                                <template #content> 
                                   <div class="row">
                                       <div class="col-7">
                                            Please login to add this item to your basket.
                                       </div>
                                       <div class="col-5">
                                           <q-btn 
                                           color="green-9" 
                                           class="text-white q-pa-sm" 
                                           label="Login/Sign Up" 
                                           dense
                                           no-caps
                                           />
                                       </div>
                                   </div>
                                </template>
                            </Popper>  
                           
                        </div>
                      </q-card-section> 
                  </q-card-section> 
 
              </q-card>
          </div>
    </div> 
</template>
<script>
import Popper from "vue3-popper";
export default {
    components:{Popper},
    
}
</script>
<style scoped>

.my-box:hover { 
  border:1px solid green;
  border-box: box-sizing;
}

:deep(.popper) {
    background: #FFF;
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
    background: #FFF;
    left:-5px;
  }

  :deep(.popper:hover),
  :deep(.popper:hover > #arrow::before) {
    background: #FFF;
  }
</style> 