<template>
  <q-layout view="lHh Lpr lFf"> 
        <header-site/>
        <content-header/>
        <q-page-container style="background:#F7F7F7;"> 
            <router-view />
            <center>
            <div class="text-caption text-grey-7 q-pb-lg">
              We're always working to get the most accurate information. 
              <a href="#" style="text-decoration:none;" class="text-blue-5">Let us know </a>
              if you come across anything that's outdated!
            </div>
            </center>
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
