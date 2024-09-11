<template>
  <div v-if="item.isVisible">
    <h2>{{ item.name }}</h2>
    <p>{{ item.price }}</p>
    <button @click="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  props: {
    item: Object
  },
  methods: {
    addToCart() {
      console.log('Adding to cart:', this.item.name, this.item.price);
      this.$emit('add-to-cart', this.item);
    }
  }
}
</script>
