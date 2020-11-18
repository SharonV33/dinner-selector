<template>
    <div>
        <h2>ingredients</h2>
        <ul>
            <li v-for="ingredient in singleDish.ingredients" :key="ingredient.name">
                {{ingredient.name}} {{ingredient.amount}}
            </li>
        </ul>
        <hr />
        <h2>steps</h2>
        <ul>
            <li v-for="steps in singleDish.steps" :key="steps.name">
                {{steps.name}}
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "recipieCard",
        props: ["singleDish"]
    }
</script>

<style scoped>
    ul {
        padding-left: 20px;
    }

</style>