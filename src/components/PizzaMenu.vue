<!-- PizzaBox.vue -->
<template>
      <div v-for="pizza of menu" :key="pizza.id">
        <PizzaItem :pizza=pizza />
      </div>
  </template>
  
  <script>
  import PizzaItem from './PizzaItem.vue';
  
  export default {
    name: 'PizzaMenu',
    props: {
      menu: Array,
    },
    components:{
        PizzaItem
    }
  };
  </script>
  
  <style scoped>
  
  </style>
  