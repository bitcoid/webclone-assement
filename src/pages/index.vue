<template>
    <div class="my-Oxygen">
        <bread-crumb/> 
             
        <q-chip flat color="white" dense size="14px" class="q-py-lg q-pa-md">
        <q-icon name="verified" style="color:#00B14F"/> 
        <span class="text-bold q-pl-sm" style="color:#00B14F"> Preferred Merchant </span>
        </q-chip>

        <q-list style="margin-top:-20px;">
            <q-item>
                <q-item-section>
                    <q-item-label class="text-h4 text-bold q-px-xs">Do Yan Seafood - Sumbersekar</q-item-label>
                    <q-item-label class="q-py-xs">
                        <q-badge color="white" 
                            class="text-black text-subtitle2" 
                            label="Seafood , Snack"
                            />
                        
                    </q-item-label>
                    <q-item-label class="q-px-xs">
                        <div class="row">
                            <div class="col-1">
                                <q-icon name="star" color="orange"></q-icon> 4.7
                            </div>
                            <div class="col-3">
                                664.1 km   
                            </div>
                        </div>
                        
                    </q-item-label> 
                    <q-item-label style="top:110px; position:absolute;"> 
                            <q-badge color="white" class="text-black text-subtitle2 text-bold" label="Opening Hours" />
                            <q-badge color="white" class="text-black text-subtitle2" label="Today Closed" /> 
                            <q-chip  square  color="red" text-color="white" label="Closed" />
                            <div class="q-py-sm">
                                <q-img 
                                    src="https://food.grab.com/static/images/icons/icon-promo-tag.svg"
                                    style="width:25px;"
                                >
                                </q-img>
                                DISKONKILATJAN 50% | HEMAT40 40% | HEMAT35 35% 
                                <q-btn flat no-caps color="blue" class="text-bold" label="See details" />
                                <br>
                                <q-icon name="info_outline" size="25px" color="grey" /> 
                                Order fee of Rp3.000 applies for this restaurant.
                            </div> 
                            <div class="row">
                                <q-select                                      
                                    outlined  
                                    v-model="model" 
                                    :options="options" 
                                    label="Delivery Date : Today"  
                                    dense
                                    :options-dense="denseOpts"
                                    class="col-4"
                                >
                                    <template v-slot:prepend>
                                        <q-icon name="date_range" />
                                    </template> 
                                </q-select>
                                <q-select                                      
                                    outlined  
                                    v-model="model" 
                                    :options="options" 
                                    label="Delivery Time : Now"  
                                    dense
                                    :options-dense="denseOpts"
                                    class="col-4 q-px-sm"
                                >
                                    <template v-slot:prepend>
                                        <q-icon name="access_time" />
                                    </template> 
                                </q-select> 
                            </div> 
                             
                            <!--tab na intersect-->  
                           <div class="row">
                               <div class="col-11">
                                   <tab-nav />
                               </div>
                           </div>

                    </q-item-label> 
                </q-item-section> 
            </q-item>
        </q-list>

       
       
        
    </div>
</template>
<script> 
import BreadCrumb from 'components/BreadCrumb'
import TabNav from 'components/TabNav'
export default {
    components:{BreadCrumb, TabNav}
}
</script>

