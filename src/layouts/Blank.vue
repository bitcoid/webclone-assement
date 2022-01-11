<template>
  <q-layout view="lHh Lpr lFf"> 
      <router-view /> 
  </q-layout>
</template>

<script>
import Header from './Header'
import Footer from './Footer'
export default {
    component:{Header,Footer}
}
</script>
