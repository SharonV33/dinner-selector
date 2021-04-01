<template>
    <div class="dishes">
        <!--for each dish in listofdishes, repeat this div-->
        <div id="dish" v-for="dish in listOfDishes" :key="dish.id">
            <!--bind dish array to single-dish-->
            <single-dish v-bind:dish="dish" :key="dish.id" :id="dish.id"/>
        </div>
        <button v-on:click="randomDish" class="btn">random</button>
    </div>
</template>

<script>
    import SingleDish from "./singleDish"

    export default {
        name: "Dishes",
        components: {
            SingleDish
        },
        props: {
            listOfDishes: { type: Array },

        },
        methods: {
        randomDish () {

            const randomNumber = Math.floor(Math.random() * this.listOfDishes.length)
            this.listOfDishes.forEach(dish => dish.isRandom = false)
            // console.log(this.listOfDishes)
            this.listOfDishes.forEach(dish => {if (dish.id === randomNumber) {
                dish.isRandom = true
            }})



            return this.listOfDishes[randomNumber]
        }
        }
    }
</script>

<style scoped>

    .dishes {
        display: flex;
        flex-wrap: wrap;
        height: 100%;
    }

    .dishes > div {
        width: 50%;
        height: 3em;
    }

    .btn {
        display: inline-block;
        align-self: flex-end;
        border: none;
        background: #555;
        color: #fff;
        padding: 12px 20px;
        width: 100%;
    }
    .btn:hover {
        background: #666;
    }

</style>
