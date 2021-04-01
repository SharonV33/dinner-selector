<template>
    <div>
        <div v-if="dish.isRandom" class="chosenDish" id="dish">
            <section class="title">
                <p class="dish-title">{{dish.title}}</p>
            </section>
        </div>

        <div v-else class="single-dish" id="dish">
            <section class="title">
                <p class="dish-title">{{dish.title}}</p>
            </section>
        </div>
    </div>
</template>

<script>

    export default {
        name: "singleDish",
        props: ["dish"]
    }
</script>

<style scoped>
    .single-dish {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
    }
    .title {
        width: 100%;
        display: grid;
        grid-template-columns: auto 10%;
    }
    span {
        border: 1px solid darkgrey;
        padding: 5px 10px;
        border-radius: 50px;
        height: 32px;
        justify-self: end;
    }
    .chosenDish {
        background-color: red;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
        display: flex;
        flex-direction: column;
    }
    #info {
        align-self: flex-start;
    }
    .hide {
        display: none;
    }
</style>