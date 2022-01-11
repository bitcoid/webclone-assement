<template>
  <q-layout view="lHh Lpr lFf"> 
      <header-site/>
        <q-page-container>
            <router-view class="q-ma-lg q-pa-lg"/> 
        </q-page-container>
      <footer-site/> 
  </q-layout>
</template>

<script>
  import HeaderSite from './HeaderSite'
  import FooterSite from './FooterSite'
  export default {
    components:{ HeaderSite, FooterSite}
  }
</script>
