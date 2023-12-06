<template>
  <div id="app">
    <!-- Step 3: Use the components -->
    <MyHeader restaurantName="Your Pizza Place" />
    <PizzaMenu :menu="menu" />
  </div>
</template>

<script>
// Step 1: Import the components
import MyHeader from './components/MyHeader.vue';
import PizzaMenu from './components/PizzaMenu.vue';

export default {
  name: 'App',

  // Step 2: Register the components
  components: {
    MyHeader,
    PizzaMenu,
  },

  data() {
    return {
      menu: [],
    };
  },

  methods: {
    // Promises
    async fetchMenu(){
      const res = await fetch('https://pizza-r3s2.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.menu = await this.fetchMenu();
  }

  // data() => this.data books
  // method => this.method => fetchbook
  // life cycle hooks created() => call our method here

}
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}

.container {
  max-width: 800px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div {
  margin-bottom: 0.5em;
}
</style>
