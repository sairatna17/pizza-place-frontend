<!-- MyHeader.vue -->
<template>
    <div>
      <h1>{{ restaurantName }} </h1>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MyHeader',
    props: {
      restaurantName: String,
    },
  };
  </script>
  
  <style scoped>
  div{
    text-align: center;
  }
  </style>
  