<template>
    <div>
        <h2>当前用户：{{ userName }}</h2>
        <p>全名:{{ firstName + lastName}}</p>
        </div>
        </template>

        <script setup lang="ts">
        import{ ref } from 'vue'
        const userName = ref<string>('张三')
        console.log(userName.value)
        const firstName = ref<string>('张')
        const lastName = ref<string>('三')
        </script>