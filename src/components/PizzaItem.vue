<!-- PizzaItem.vue -->
<template>
    

  <div  :class="pizza.vegetarian ? 'green': 'red' ">

    <h2>{{ pizza.name }}</h2>
    <h4>Sizes:</h4>
    <ul>
      <li v-for="size in pizza.sizes" :key="size.size">
        {{ size.size }} - ${{ size.price }}
      </li>
    </ul>
    <h4>Toppings: {{ pizza.toppings.join(', ') }}</h4>
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

h2{
  margin: 2px;
}

h4{
    margin: 2px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 4px 0;
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