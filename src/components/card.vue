<template>
    <div class="row my-Oxygen" style="margin-left:-10px;">
          <div class="col-4 q-pa-sm" v-for="n in 5" :key="n">
              <q-card 
                  class="my-card"
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
                           <q-btn color="green" class="text-white" icon="add" dense/>
                        </div>
                      </q-card-section> 
                  </q-card-section> 
 
              </q-card>
          </div>
    </div> 
</template>
<script>
export default {
    
}
</script>