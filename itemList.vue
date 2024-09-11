<template>
  <div>
    <Item
      v-for="item in filteredItems"
      :key="item.id"
      :item="item"
      @add-to-cart="handleAddToCart"
    />
  </div>
</template>

<script>
import Item from './itemList.vue';

export default {
  components: { Item },
  props: {
    items: Array
  },
  computed: {
    filteredItems() {
      return this.items.filter(item => item.isVisible);
    }
  },
  methods: {
    handleAddToCart(item) {
      console.log('Item added to cart:', item);
    
    }
  }
}
</script>
