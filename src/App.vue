<template>
  <div id="app">
    <h1>Deja tu Comentario</h1>
    <CommentForm @submit-comment="addComment"/>
    <CommentList :comments="comments"/>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import CommentForm from './CommentForm.vue';
import CommentList from './CommentList.vue';

const comments = ref([]);

function addComment(newComment) {
  // TODO: Implementa esta función para añadir un nuevo comentario al array comments.
}
</script>