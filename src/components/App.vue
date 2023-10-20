<template>
    <div>
      <router-view></router-view>
      <button @click="showCounter">Показать Counter</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      showCounter() {
        this.$router.push('/show-counter');
      },
    },
  };
  </script>
  