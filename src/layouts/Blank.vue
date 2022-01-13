<template>
  <q-layout view="lHh Lpr lFf"> 
        <header-site/>
        <content-header/>
        <q-page-container style="background:#F7F7F7;"> 
            <router-view /> 
        </q-page-container>
        <footer-site/>
  </q-layout>
</template>

<script>
  import HeaderSite from './HeaderSite'
  import FooterSite from './FooterSite'
  import ContentHeader from './ContentHeader'
  export default {
    components:{ HeaderSite, FooterSite, ContentHeader}
  }
</script>
