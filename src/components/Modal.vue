<script setup>
const props = defineProps({
  header: String,
  theme: String,
});
</script>
<template>
  <div class="backdrop">
    <div class="modal" :class="{ red: theme === 'red' }">
      <h1>{{ props.header }}</h1>
      <p>{{ props.theme }}</p>
    </div>
  </div>
</template>
<style>
.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}
.backdrop {
  left: 0;
  top: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
.modal h1 {
  color: mediumturquoise;
  border: none;
  padding: 0;
}
.modal.red {
  background: crimson;
  color: white;
}
.modal.red h1 {
  color: white;
}
</style>
