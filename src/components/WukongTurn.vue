
<template>
  <div class="story-container">
    <h2 class="name">{{ name }}</h2>
    <h2 class="title">{{ currentForm }}</h2>
    <h2 class="description">{{ description }}</h2>
    <button @click="toggleForm" class="toggle-button">切换形态</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const name = ref<string>('孙悟空');
const forms = ['齐天大圣', '斗战胜佛'];
const currentForm = ref<string>(forms[0]);
const description = ref<string>('在西游记中，孙悟空是一个顽皮无畏、机智聪明的角色');

const toggleForm = () => {
  currentForm.value = currentForm.value === forms[0] ? forms[1] : forms[0];
};
</script>

<style scoped>
div {
  background-color: white;
  border-radius: 10px;
  box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.5);
  margin: 10px;
  padding: 10px;
}

.name {
  font-size: 2em;
  color: gold;
  text-align: center;
}

.title {
  font-size: 1.5em;
  color: black;
  text-align: center;
}

.description {
  font-size: 1em;
  color: #352f2f;
  text-align: center;
}

.toggle-button {
  margin-top: 10px;
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.toggle-button:hover {
  background-color: #45a049;
}
</style>


