<template>
    <div>
        <!--for each dish in listofdishes, repeat this div-->
        <div id="dish" v-for="dish in listOfDishes" :key="dish.id">
            <!--bind dish array to single-dish-->
            <single-dish v-bind:dish="dish" :key="dish.id"/>
        </div>
        <button v-on:click="randomDish" class="btn">random</button>
    </div>
</template>

<script>
    import SingleDish from "./singleDish";

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
            const randomNumber = Math.floor(Math.random() * this.listOfDishes.length);
            this.listOfDishes.forEach(dish => dish.isRandom = false);
            this.listOfDishes.forEach(dish => dish.isRandom = dish.id === randomNumber);
            return this.listOfDishes[randomNumber];
        }
        }
    }
</script>

<style scoped>
    .btn {
        display: inline-block;
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
