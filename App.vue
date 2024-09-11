<template>
  <div class="container">
    <h1>Item List</h1>
    <div class="item-list">
      <div v-for="product in products" :key="product.id" class="product">
        <p>{{ product.name }}</p>
        <p>Price: ${{ product.price }}</p>
        <button @click="addToCart(product)">Add to Cart</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { name: "Product 1", price: 100, isVisible: true },
        { name: "Product 2", price: 150, isVisible: true },
        { name: "Product 3", price: 200, isVisible: true },
        { name: "Product 4", price: 250, isvisible: true },
        { name: "Product 5", price: 300, isVisible: false },
      ],
    };
  },
  methods: {
    addToCart(product) {
      console.log(`${product.name} has been added to the cart.`);
    },
  },
};
</script>
