<template>
    <form @submit.prevent="submitComment">
      <input v-model="author" placeholder="Tu nombre"/>
      <textarea v-model="content" placeholder="Tu comentario"></textarea>
      <button type="submit">Enviar</button>
    </form>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const emit = defineEmits(['submit-comment']);
  
  const author = ref('');
  const content = ref('');
  
  function submitComment() {
    emit('submit-comment', { author: author.value, content: content.value });
    author.value = '';
    content.value = '';
  }
  </script>