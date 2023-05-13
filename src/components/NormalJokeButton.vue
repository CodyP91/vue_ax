<template>
  <button @click="setFormat('normal')">Normal Joke</button>
</template>

<script>
export default {
  methods: {
    setFormat(format) {
      this.$emit('format', format);
    },
  },
};
</script>

<style scoped>

</style>
