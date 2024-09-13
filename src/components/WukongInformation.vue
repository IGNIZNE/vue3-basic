
<template>
<div class="story-container">
<h2>{{ name }}</h2>
<h2>{{ title }}</h2>
<h2>{{ description }}</h2>    
</div>

</template>

<script setup lang="ts">
import { ref } from 'vue';
const name = ref<string>('孙悟空');
const title = ref<string>('齐天大圣');
const description = ref<string>('在西游记中，孙悟空是一个顽皮无畏、机智聪明的角色');
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
</style>

