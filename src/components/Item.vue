<template>
    <div v-if="isVisible" class="item-container">
      <p class="item-name">Name: {{ item.name }}</p>
      <p class="item-price">Price: ${{ item.price }}</p>
      <button class="add-to-cart-btn" @click="addToCart">Add to Cart</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Item',
    props: {
      item: {
        type: Object,
        required: true
      }
    },
    data() {
      return {
        isVisible: true
      }
    },
    methods: {
      addToCart() {
        console.log(`Added to cart: Name - ${this.item.name}, Price - $${this.item.price}`);
        this.$emit('add-to-cart', this.item);
      }
    }
  }
  </script>
  
  <style scoped>
  .item-container {
    border: 1px solid #ddd;
    padding: 16px;
    border-radius: 8px;
    background-color: transparent;
    max-width: 300px;
    margin: 20px auto;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .item-container:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
  }
  
  .item-name {
    font-size: 18px;
    font-weight: bold;
    margin: 0 0 8px 0;
  }
  
  .item-price {
    font-size: 16px;
    color: #333;
    margin: 0 0 16px 0;
  }
  
  .add-to-cart-btn {
    background-color: #ff4d4d;
    color: white;
    border: none;
    border-radius: 4px;
    padding: 10px 20px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
  }
  
  .add-to-cart-btn:hover {
    background-color: #ff6666;
  }
  </style>
  