<template>
    <div>
<p :class="pClass">这是一段文字</p>
<button @click="toggleClass">切换样式</button>
    </div>  
    </template>

    <script setup lang ="ts">
    import { normalize } from 'path';
import { ref } from 'vue'

    const isHighLight = ref<boolean>(false)

    const pClass = ref<{ [key: string]: boolean}>({
        isHighLight : isHighLight.value,
        normalize : !isHighLight.value
    })

const toggleClass = () => {
    isHighLight.value = !isHighLight.value
    pClass.value = {
        isHighLight : isHighLight.value,
        normalize : !isHighLight.value
    }
}


</script>


<style scoped>
.isHighLight{
    color: red;
}
.mormal{
    color: black;
}
</style>