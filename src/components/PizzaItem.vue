<!-- PizzaItem.vue -->
<template>
    

  <div  :class="pizza.vegetarian ? 'green': 'red' ">

    <h2>{{ pizza.name }}</h2>
    <h4>{{ pizza.vegetarian }}</h4>
    
  </div>
</template>
  
  <script>
  export default {
    name: 'PizzaItem',
    props: {
      pizza: Array,
    },
  };
  </script>
  
  <style scoped>
  .green{
    background-color: green;
}

h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}

.red{
background-color: orangered !important;

}


</style>