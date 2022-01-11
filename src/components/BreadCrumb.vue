<template>
    <q-breadcrumbs class="text-brown my-Oxygen q-pl-lg" >
      <template v-slot:separator>
        <q-icon
          size="1.5em"
          name="arrow_forward_ios"
          color="primary"
        />
      </template>

      <q-breadcrumbs-el>
            <span class="text-subtitle1 text-bold text-blue-4">Home</span>
      </q-breadcrumbs-el>
      <q-breadcrumbs-el>
            <span class="text-subtitle1 text-bold text-blue-4">Restaurant</span>
      </q-breadcrumbs-el>
      <q-breadcrumbs-el>
            <span class="text-subtitle1">Do Yan Seafood - Sumbersekar</span>
      </q-breadcrumbs-el>
    </q-breadcrumbs>
</template>
<script>
export default {
    
}
</script>