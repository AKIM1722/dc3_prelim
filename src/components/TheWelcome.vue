<template>
  <div id="app">
    <h1>Conditional Rendering and Computed Properties in Vue</h1>
    
    <h2>Items List</h2>
    <ul>
      <li v-for="item in filteredItems" :key="item.id">
        <span v-if="item.isActive">{{ item.name }} - Active</span>
        <span v-else>{{ item.name }} - Inactive</span>
      </li>
    </ul>

    <h2>Active Items Count</h2>
    <p>Total Active Items: {{ activeItemsCount }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { id: 1, name: 'Item 1', isActive: true },
        { id: 2, name: 'Item 2', isActive: false },
        { id: 3, name: 'Item 3', isActive: true },
        { id: 4, name: 'Item 4', isActive: false },
      ],
    };
  },
  computed: {
    filteredItems() {

      return this.items.filter(item => item.isActive || !item.isActive);
    },
    activeItemsCount() {
  
      return this.items.filter(item => item.isActive).length;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
