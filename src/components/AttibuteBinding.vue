<template>
    <div>

        <button :disabled= "isDisabled">点击</button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const isDisabled = ref<boolean>(false)
</script>

