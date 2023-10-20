<template>
    <div class="modal">
      <div class="modal-content">
        <h2>Counter Value</h2>
        <p>{{ counter }}</p>
        <button @click="$router.push('/')">Закрыть</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      counter: Number,
    },
  };
  </script>
  
  <style scoped>
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 999;
  }
  
  .modal-content {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
  }
  </style>
  