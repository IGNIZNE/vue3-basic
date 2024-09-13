<template>
<div class="equipmentManager">  
    <h2>装备管理</h2>  
    <!-- 表单部分 -->  
    <div>  
      <input id="equipmentName" v-model="newEquipment" type="text" placeholder="输入装备名称" />  
      <button @click="addEquipment">添加装备</button>  
    </div>  
    <!-- 装备列表部分 -->  
    <ul>  
      <li v-for="equipment in equipments" :key="equipment.id">  
        {{ equipment.name }}  
        <button @click="removeEquipment(equipment.id)">删除</button>  
      </li>  
    </ul>  
  </div>  
</template>

  <script setup lang="ts">  
  import { ref } from 'vue';  
  
  interface Equipment {  
    id: number;  
    name: string;  
  }  
  
  const equipments = ref<Equipment[]>([]);  
  const newEquipment = ref<string>('');

    const addEquipment = () => {  
  if (newEquipment.value.trim() !== '') {  
    equipments.value.push({  
      name: newEquipment.value,  
      id: 0,  
    });  
  newEquipment.value = '';
  }  
};  

const removeEquipment = (id: number) => {  
  equipments.value.splice(id, 1);  
};  
</script>  

<style scoped>  
.equipmentManager {  
  max-width: 400px;  
  margin: 0 auto;  
  padding: 20px;  
  border: 1px solid #ccc;  
  border-radius: 8px;  
}  


input[type="text"] {
    width: calc(100% - 22px);
    padding: 10px;
    margin-top: 5px;
    margin-bottom: 15px;
    box-sizing: border-box;
}

button {
    background-color: #1a73e8;
    color: white;
    border: none;
    padding: 5px 10px;
    margin-left: 5px;
    cursor: pointer;
}

ul {
    list-style-type: none;
    padding: 0;
}


li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 8px;
    border-bottom: 1px solid #eee;
}

button:hover {
    background-color: #155ab6;
}
</style>


