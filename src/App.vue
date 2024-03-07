<template>
  <div id="app">
    <h1>Deja tu Comentario</h1>
    <CommentForm @submit-comment="addComment"/>
    <CommentList :comments="comments"/>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import CommentForm from './components/ComponentForm.vue';
import CommentList from './components/CommentList.vue';

const comments = ref([]);

function addComment(newComment) {
  comments.value.push(newComment)
}
</script>