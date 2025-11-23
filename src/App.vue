<script setup>
import { ref } from 'vue';
import Modal from './components/Modal.vue';
const title = ref('My first Vue app');
const name = ref(null);
const appText = 'Mám ráda červenou?';
const red = ref('red');

function handleClick() {
  console.log(name.value);
  name.value.classList.add('active');
}
</script>

<template>
  <h1>{{ title }}</h1>
  <Modal :header="appText" :theme="'red'" />
  <button @click="handleClick">Click me</button>

  <input type="text" ref="name" />
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
</style>
