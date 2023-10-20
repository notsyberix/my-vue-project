<template>
    <div>
      <button @click="increment">+1</button>
      <button @click="decrement">-1</button>
      <p>Counter: {{ counter }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        counter: 0,
      };
    },
    methods: {
      increment() {
        this.counter++;
      },
      decrement() {
        this.counter--;
      },
    },
  };
  </script>
  