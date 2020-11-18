<template>
    <div>
        <div v-if="dish.isRandom" class="chosenDish">
            <section class="title">
                <p class="dish-title">{{dish.title}}</p>
                <span v-on:click="hide" class="infoButton">i</span>
            </section>
            <section class="hide" id="info">
                <recipieCard v-bind:singleDish = "dish"/>
            </section>
        </div>

        <div v-else class="single-dish">
            <section class="title">
                <p class="dish-title">{{dish.title}}</p>
                <span v-on:click="hide" class="infoButton">i</span>
            </section>
            <section class="hide" id="info">
                <recipieCard v-bind:singleDish = "dish"/>
            </section>
        </div>
    </div>
</template>

<script>
    import recipieCard from "./recipieCard";

    export default {
        name: "singleDish",
        components: {
            recipieCard
        },
        props: ["dish"],
        methods: {
            hide() {
                let element = document.getElementById("info");
                element.classList.toggle("hide");
            }
        }
    }
</script>

<style scoped>
    .single-dish {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
        display: flex;
        flex-direction: column;
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