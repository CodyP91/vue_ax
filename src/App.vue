<template>
  <div class="app-container">
    <JokeGenerator />
  </div>
</template>

<script>
import JokeGenerator from "@/components/JokeGenerator.vue";

export default {
  name: "App",
  components: {
    JokeGenerator,
  },
};
</script>

<style>
.app-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>
