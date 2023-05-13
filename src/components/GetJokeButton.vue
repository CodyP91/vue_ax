<template>
    <button @click="getJoke">Get New Joke</button>
  </template>
  
  <script>
  import axios from 'axios';
  
  export default {
    name: 'GetJokeButton',
    methods: {
      getJoke() {
        axios
          .get('https://ron-swanson-quotes.herokuapp.com/v2/quotes')
          .then(response => {
            this.$emit('new-joke', response.data[0]);
          })
          .catch(error => {
            console.error('Error fetching joke:', error);
          });
      },
    },
  };
  </script>
  