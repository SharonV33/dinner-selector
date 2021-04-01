<template>
  <div id="app">
    <h1>Pick a random dish</h1>
    <Dishes v-bind:listOfDishes = "listOfDishes"/>
  </div>
</template>

<script>

import Dishes from './components/Dishes.vue'

export default {
  name: 'App',
  components: {
    Dishes
  },
  data() {
    return {
      listOfDishes: [
        {
          id: 0,
          title: "pasta",
          isRandom: false
        },
        {
          id: 1,
          title: "Hamburgers",
          isRandom: false
        },
        {
          id: 2,
          title: "Snackbar",
          isRandom: false
        },
        {
          id: 3,
          title: "Pancakes",
          isRandom: false
        },
        {
          id: 4,
          title: "Bami",
          isRandom: false
        },
        {
          id: 5,
          title: "Nasi",
          isRandom: false
        },
        {
          id: 6,
          title: "Chinese omelet",
          isRandom: false
        },
        {
          id: 7,
          title: "Chicken wraps",
          isRandom: false
        },
        {
          id: 8,
          title: "Falafel wraps",
          isRandom: false
        },
        {
          id: 9,
          title: "Rice with chicken/sausage",
          isRandom: false
        },
        {
          id: 10,
          title: "Chili",
          isRandom: false
        },
        {
          id: 11,
          title: "Lasagna",
          isRandom: false
        },
        {
          id: 12,
          title: "Kapsalon",
          isRandom: false
        },
        {
          id: 13,
          title: "Chili couscous with shoarma",
          isRandom: false
        },
        {
          id: 14,
          title: "Paella",
          isRandom: false
        },
        {
          id: 15,
          title: "Beef shanghai",
          isRandom: false
        },
        {
          id: 16,
          title: "Quesedillas",
          isRandom: false
        },
        {
          id: 17,
          title: "Kip Siam",
          isRandom: false
        },
        {
          id: 18,
          title: "Burito's",
          isRandom: false
        },
      ]
    }
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
    display: flex;
    justify-content: center;
  }
  #app {
    margin-top: 2em;
    height: 100%;
    border: 1px solid #717171;
    margin-bottom: 40px;
    width: 50vw;
  }
  h1 {
    text-align: center;
    margin: 10px;
  }

</style>
