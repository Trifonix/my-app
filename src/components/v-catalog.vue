<template>
  <div class="v-catalog">
    <h1>Hello i am Catalog!</h1>
    <vCatalogItem />
  </div>
</template>

<script>

import vCatalogItem from './v-catalog-item.vue'
export default {
  name: 'v-catalog',
  components: {
    vCatalogItem
  },
  props: {},
  data () {
    return {}
  }
}
</script>

<style></style>
