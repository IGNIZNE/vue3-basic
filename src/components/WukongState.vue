<!-- 
<template>
    <p>血量：{{ currentHP }} / {{ totalHP }} ({{ hpPercentage }}%)</p>
    <div class="progress-bar" 
        :style="{ width: `${hpPercentage}%`, backgroundColor: getBackgroundColor(hpPercentage) }"></div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue';

const totalHP = ref<number>(100);
const hpPercentage = ref<number>(70);
const currentHP = computed(() => {
    return totalHP.value * hpPercentage.value / 100;
});

const getBackgroundColor = (percentage: number): string => {
    if (percentage > 50) {
        return 'green';
    } else if (percentage >= 25) {
        return 'yellow';
    } else {
        return 'red';
    }
};
</script>

<style scoped>
.progress-bar {
    height: 20px;
    background-color: green; 
    transition: width 0.3s ease, background-color 0.3s ease;
}
</style>
 -->
 <!-- <template>  
    <div>  
        <p>血量：{{ currentHP }} / {{ totalHP }} ({{ hpPercentage }}%)</p>  
        <div class="progress-bar"   
            :style="{ width: `${hpPercentage}%`, backgroundColor: getBackgroundColor(hpPercentage) }"></div>  
        <button @click="decreaseHP" class="mt-2">减少 10% 血量</button>  
    </div>  
</template>  

<script setup lang="ts">  
import { ref, computed } from 'vue';  

const totalHP = ref<number>(100);  
const hpPercentage = ref<number>(70); // 初始为 70%  
const currentHP = computed(() => {  
    return totalHP.value * hpPercentage.value / 100;  
});  

// 减少血量的函数  
const decreaseHP = () => {  
    if (hpPercentage.value > 0) {  
        hpPercentage.value = Math.max(hpPercentage.value - 10, 0); // 每次点击减少 10%，至少为 0%  
    }  
};  

const getBackgroundColor = (percentage: number): string => {  
    if (percentage > 70) {  
        return 'green';  
    } else if (percentage > 40) {  
        return 'yellow';  
    } else {  
        return 'red';  
    }  
};  
</script>  

<style scoped>  
.progress-bar {  
    height: 20px;  
    background-color: green;   
    transition: width 0.3s ease, background-color 0.3s ease;  
}  

button {  
    background-color: #007BFF;  
    color: white;  
    border: none;  
    padding: 10px 15px;  
    border-radius: 5px;  
    cursor: pointer;  
}  

button:hover {  
    background-color: #0056b3;  
}  
</style> -->
<template>  
    <div>  
        <p>血量：{{ currentHP }} / {{ totalHP }} ({{ hpPercentage }}%)</p>  
        <div class="progress-bar"   
            :style="{ width: `${hpPercentage}%`, backgroundColor: getBackgroundColor(hpPercentage) }"></div>  
        <button @click="decreaseHP" class="mt-2">减少 10% 血量</button>  
        <button @click="increaseHP" class="mt-2 ml-2">增加 10% 血量</button>  
    </div>  
</template>  

<script setup lang="ts">  
import { ref, computed } from 'vue';  

const totalHP = ref<number>(100);  
const hpPercentage = ref<number>(70); // 初始为 70%  
const currentHP = computed(() => {  
    return totalHP.value * hpPercentage.value / 100;  
});  

// 减少血量的函数  
const decreaseHP = () => {  
    if (hpPercentage.value > 0) {  
        hpPercentage.value = Math.max(hpPercentage.value - 10, 0); // 每次点击减少 10%，至少为 0%  
    }  
};  

// 增加血量的函数  
const increaseHP = () => {  
    if (hpPercentage.value < 100) {  
        hpPercentage.value = Math.min(hpPercentage.value + 10, 100); // 每次点击增加 10%，最多为 100%  
    }  
};  

const getBackgroundColor = (percentage: number): string => {  
    if (percentage > 70) {  
        return 'green';  
    } else if (percentage > 40) {  
        return 'yellow';  
    } else {  
        return 'red';  
    }  
};  
</script>  

<style scoped>  
.progress-bar {  
    height: 20px;  
    background-color: green;   
    transition: width 0.3s ease, background-color 0.3s ease;  
}  

button {  
    background-color: #007BFF;  
    color: white;  
    border: none;  
    padding: 10px 15px;  
    border-radius: 5px;  
    cursor: pointer;  
}  

button:hover {  
    background-color: #0056b3;  
}  

.mt-2 {  
    margin-top: 0.5rem;  
}  

.ml-2 {  
    margin-left: 0.5rem;  
}  
</style>