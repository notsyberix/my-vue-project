<template>
    
    <div class="chat-container">
      <h1>Чат</h1>
      <div class="chat-messages">
        <div v-for="message in messages" :key="message.id" class="message">
          {{ message.text }}
        </div>
      </div>
      <div class="chat-input">
        <input v-model="newMessage" @keyup.enter="sendMessage" placeholder="Введите сообщение" />
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        messages: [],
        newMessage: "",
      };
    },
    methods: {
      sendMessage() {
        if (this.newMessage.trim() !== "") {
          this.messages.push({ id: Date.now(), text: this.newMessage });
          this.newMessage = "";
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .chat-container {
    padding: 20px;
  }
  
  .message {
    background-color: #f0f0f0;
    margin: 10px 0;
    padding: 10px;
    border-radius: 5px;
  }
  
  .chat-input input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  </style>
  