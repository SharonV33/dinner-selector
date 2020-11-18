<template>
  <div id="application">
    <h1>Pick a random dish</h1>
    <Dishes v-bind:listOfDishes = "listOfDishes"/>
  </div>
</template>

<script>

  import Dishes from '../components/Dishes.vue'

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
            isRandom: false,
            ingredients: [{
              name: 'sauce',
              amount: '100ml'
            }, {
              name: 'pasta',
              amount: '500g'
            }],
            steps: [{
              id: 1,
              name: "cook pasta",
            },
              {
                id: 2,
                name: "add sauce"
              }]
          },
          {
            id: 1,
            title: "hamburger",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 2,
            title: "snackbar",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 3,
            title: "pancakes",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 4,
            title: "bami",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 5,
            title: "nasi",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 6,
            title: "chinese omelet",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 7,
            title: "chicken wraps",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 8,
            title: "falafel wraps",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 9,
            title: "rice with chicken and sausage",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 10,
            title: "chili",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 11,
            title: "lasagna",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 12,
            title: "kapsalon",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 13,
            title: "chili couscous with shoarma",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 14,
            title: "paella",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 15,
            title: "beef shanghai",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          },
          {
            id: 16,
            title: "quesedillas",
            isRandom: false,
            ingredients: [{
              name: 'salt',
              amount: '100g'
            }, {
              name: 'pepper',
              amount: '200g'
            }]
          }
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
    background: #b2b2b2;
  }
  #application {
    width: 50%;
    margin-top: 2em;
    margin-bottom: 10em;
    border: 1px solid #717171;
    box-shadow: 1em 0.5em 0.5em #343434;
  }
  h1 {
    text-align: center;
    margin: 10px;
  }

</style>
