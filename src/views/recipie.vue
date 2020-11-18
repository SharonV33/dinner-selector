<template>
  <div class="about">
    <h1>This is an about page</h1>
    <recipieCard />
  </div>
</template>

<script>
  import recipieCard from "../components/recipieCard";

  export default {
    name: "recipie",
    components: {
      recipieCard
    },
    props: ["dish"],
    methods: {}
  }
</script>
