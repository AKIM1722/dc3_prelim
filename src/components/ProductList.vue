<template>
    <div id="app">
      <ProductList :products="products" />
    </div>
  </template>
  
  <script>
  import ProductList from './components/ProductList.vue';
  
  export default {
    name: 'App',
    components: {
      ProductList,
    },
    data() {
      return {
        products: [
          { id: 1, name: 'Product 1', price: 100},//, //image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSz9ZuhzzAR8xy995cn9cAbBnmn8ODoV8in8w&s' },
          { id: 2, name: 'Product 2', price: 150},//, //image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSrIjaQ0xgPi5FT9oRPoqfUCGibmrZOx41XZA&s' },
          { id: 3, name: 'Product 3', price: 200}//, //image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRpp7JZN_voM95GSpUBMWkJsAw4pPzrazJWOg&s' },
        ]
      }
    }
  }
  </script>
  
  <style>
  #app {
    font-family: Arial, Helvetica, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #333;
    margin-top: 60px;
    background-color: #eef2f5;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: 20px;
  }
  </style>
  encrypted-tbn0.gstatic.com