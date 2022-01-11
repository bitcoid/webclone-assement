<template>
   <div>
        <q-tabs
            v-model="tab"
            class="text-teal"
        >
            <q-tab name="mails" icon="mail" label="Mails"  />
            <q-tab name="alarms" icon="alarm" label="Alarms" />
            <q-tab name="movies" icon="movie" label="Movies" />
            <q-tab name="drama" icon="movie" label="Drama" />
        </q-tabs>

        <div class="relative-position">
                 
                <div class="example-area q-pa-lg scroll">
                    <div class="example-filler" style="height:100px;"/>
                        <q-list>
                            <q-item
                            v-for="n in 4"
                            :key="n"
                            :data-id="n"
                            class="q-my-md q-pa-sm bg-grey-3"
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
   </div>
</template>
<script> 
 
export default { 
    data(){
        return{
            tab: 'mails', 
            thresholds : ['', 'mails', 'alarms','movies','drama'] 
        }
    }, 
    methods:{
        onIntersection (entry) {
            if (entry.isIntersecting === true) {
                this.add(entry.target.dataset.id)
            } 
        },
        add (i) {
            console.log(i)  
            this.tab = this.thresholds[i]
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
  height: 300px

.example-filler
  height: 500px
</style>