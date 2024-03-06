<template>
    <div>
      <h2>Comentarios</h2>
      <ul>
        <li v-for="comment in comments" :key="comment.id">
          <strong>{{ comment.author }}</strong>: {{ comment.content }}
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps({
    comments: Array,
  });
  </script>  