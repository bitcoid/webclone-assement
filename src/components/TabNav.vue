<template>
    <div> 
        <q-tabs
                v-model="tab" 
                :class="{ 'newClass': isAddClass }" 
                v-scroll="handleScroll"  
                outside-arrows
                mobile-arrows
            >
                <q-tab name="1" label="Aigo" no-caps/>
                <q-tab name="2" label="Chingu" no-caps />
                <q-tab name="3" label="Seerameon Ikan" no-caps />
                <q-tab name="4"  label="Samjang Gami ( Extra Pedas )" no-caps />
                <q-tab name="5" label="Sea Monster" no-caps />
                <q-tab name="6" label="Omo" no-caps />
                <q-tab name="7" label="Saranghaeyo" no-caps />
                <q-tab name="8" label="Chaeso" no-caps /> 
                <q-tab name="9" label="Drink (Ice / Hot)" no-caps />
                <q-tab name="10" label="Addon" no-caps /> 
            </q-tabs>  
            <q-tab-panel>
            <div style="width:100%;"> 
                <div class="example-area q-pa-lg">
                    <div class="example-filler" style="height:20px;"/>
                        <q-list>
                            <q-item
                            v-for="n in 10"
                            :key="n"
                            :data-id="n"
                            class="q-my-md q-pa-sm"
                            v-intersection="onIntersection"
                            >
                            <q-item-section class="text-center" style="background: #ffffff">
                                <div style="height:500px;">
                                    Item #{{ n }}
                                </div>
                            </q-item-section>
                            </q-item>
                        </q-list>  

                    <div class="example-filler" /> 
                     
                </div>
            </div>
            </q-tab-panel>
   </div>
</template>
<script> 
 
export default { 
    data(){
        return{
            tab: '1', 
            thresholds : ['', '1', '2','3','4','5','6','7','8','9','10'],  
            isAddClass: false, 
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
                this.add(entry.target.dataset.id)
            } 
            console.log(entry.target.dataset.id)
        },
        add (i) { 
            this.tab = this.thresholds[i] 
            if(i > 1)
                this.isAddClass = true;
            else
                this.isAddClass = false;
        },
        handleScroll: function () {   
            if(window.scrollY > 400)
                this.isAddClass = true;
            else
                this.isAddClass = false;
            /*
            if (this.lastPosition < window.scrollY && this.limitPosition < window.scrollY) {
                this.scrolled = true;
                // move up!
            } 
            
            if (this.lastPosition > window.scrollY) {
                this.scrolled = false; 
                // move down
            }
            */
            
            //this.lastPosition = window.scrollY;
            //this.scrolled = window.scrollY > 250;
        }
    } 
}
</script>
<style lang="sass" scoped>
.example-state
  background: #ccc
  font-size: 20px
  color: #282a37
  padding: 10px
  opacity: 0.8

.example-observed
  height: 150px
  font-size: 20px
  color: #ccc
  background: #282a37
  padding: 10px

.example-area
  height: 800px

.example-filler
  height: 500px
 
</style>