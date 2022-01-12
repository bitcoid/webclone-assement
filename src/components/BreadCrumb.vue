<template>
    <q-breadcrumbs class="text-brown my-Oxygen">
      <template v-slot:separator>
        <q-icon
          size="1.2em"
          name="arrow_forward_ios"
          color="grey"
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