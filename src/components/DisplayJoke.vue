<template>
    <div>
      <p>{{ formattedJoke }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'DisplayJoke',
    data() {
      return {
        joke: '',
        format: 'normal',
      };
    },
    computed: {
      formattedJoke() {
        if (!this.joke) {
          return 'No joke available';
        }
  
        if (this.format === 'normal') {
          return this.joke.toLowerCase();
        } else if (this.format === 'snake') {
          return this.joke.replace(/ /g, '_');
        } else if (this.format === 'loud') {
          return this.joke.toUpperCase();
        } else {
          return this.joke;
        }
      },
    },
    methods: {
      updateJoke(newJoke) {
        this.joke = newJoke;
      },
      updateFormat(newFormat) {
        this.format = newFormat;
      },
    },
  };
  </script>
  