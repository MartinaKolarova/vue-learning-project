<script setup>
import { ref } from 'vue';
import Modal from './components/Modal.vue';

const appText = 'Mám ráda červenou?';
const theme = ref('ANO');

function toggleTheme() {
  theme.value = theme.value === 'ANO' ? 'NE' : 'ANO';
}
</script>

<template>
  <Modal :header="appText" :theme="theme" :onToggle="toggleTheme" />
</template>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px, solid, #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
button {
  margin: 10px;
  padding: 8px 15px;
}
</style>
