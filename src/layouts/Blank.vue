<template>
  <q-layout view="lHh Lpr lFf"> 
      <header-site/>
        <router-view /> 
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
