<template>
  <div class="v-catalog-item">
    <img class="v-catalog-item__image" :src="require('../assets/images/' + product_data.image)" alt="picture">
    <p class="v-catalog-item__name">{{product_data.name}}</p>
    <p class="v-catalog-item__price">{{product_data.price}}</p>
    <p class="v-catalog-item__about">{{product_data.about}}</p>
    <button class="v-catalog-item__add_to_cart_btn" @click="sendDataToParent">Add to cart</button>
  </div>
</template>

<script>
export default {
  name: 'v-catalog-item',
  props: {
    product_data: {
      type: Object,
      default () {
        return {}
      }
    }
  },
  data () {
    return {}
  },
  methods: {
    sendDataToParent () {
      this.$emit('hi', this.product_data.article)
    }
  }
}
</script>

<style lang="scss">
.v-catalog-item {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  align-items: center;
  flex-basis: 25%;
  box-shadow: 0 0 10px 0 grey;
  margin: 20px;
  padding: 20px;
}
.v-catalog-item__name {
  background-color: blueviolet;
  color: white;
  padding: 5px;
}
</style>
