<template>
    <div>
            <div class="row">
                <div style="width:99%; margin-top:-50px;">
                      <q-tabs
                            v-model="tab" 
                            :class="{ 'newClass q-tab__label': isAddClass }" 
                            v-scroll="handleScroll"  
                            outside-arrows
                            mobile-arrows
                        >
                            <q-tab 
                                v-for="(rows, index) in labels.filter((a) => a)"
                                :key="index"
                                :name="`${index+1}`" 
                                :label="rows" 
                                no-caps
                                class="q-pr-lg"
                                @click="goto(rows)" 
                            /> 
                        
                        </q-tabs>
                </div>
            </div>
  
                    <div class="example-area q-pa-xl">
                        <div class="example-filler" style="height:15px;"/>
                            <q-list>
                                <q-item
                                v-for="n in thresholds.filter((a) => a)"
                                :key="n"
                                :data-id="n"
                                class="q-my-md q-pa-sm"
                                v-intersection="onIntersection"
                                >
                                <q-item-section class="text-center"> 
                                    <div style="margin-bottom:30px; margin-left:-45px;">  
                                        <div class="text-h4 text-bold text-left q-pb-xl ">
                                            {{ labels[n] }} 
                                        </div>
                                        <div :ref="`${labels[n]}`"><card/></div> 
                                    </div> 
                                </q-item-section>
                                </q-item>
                            </q-list>  

                        <div class="example-filler" /> 
                        
                    </div> 
   </div>
</template>
<script> 
import card from './card'
let x = 0;
export default { 
    components:{card},
    data(){
        return{
            tab: '1', 
            labels : [
                '',
                'Aigo',
                'Chingu',
                'Seerameon Ikan',
                'Samjang Gami ( Extra Pedas )',
                'Sea Monster',
                'Omo',
                'Saranghaeyo',
                'Chaeso',
                'Drink (Ice / Hot)',
                'Addon'
            ],
            thresholds : ['','1','2','3','4','5','6','7','8','9','10'],
            isAddClass: false 
        }
    },
    created() {
        window.addEventListener("scroll", this.handleScroll);
    },
    mounted() {
        window.removeEventListener("scroll", this.handleScroll);
    },
    methods:{
        onIntersection (entry) { 
            if (entry.isIntersecting === true) { 
                this.tab = `${this.thresholds[entry.target.dataset.id]}`  
            } 
        },
        add (i) {  
            if(i > 1){
                this.isAddClass = true;
            }else{
                this.isAddClass = false;  
            } 
        },
        handleScroll: function () {   
            if(window.scrollY > 400){ 
                this.isAddClass = true; 
            }else{
                this.isAddClass = false; 
            }
        },
        goto(refName) {
            this.$refs[refName].scrollIntoView({behavior: 'smooth', block: "end", inline: "nearest"});  
        }
    } 
}
</script> 