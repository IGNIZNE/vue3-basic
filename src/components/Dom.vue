<!-- <template>  
    <div class="scroll-demo">  
      <button @click="scrollToSkills">滚动到技能展示</button>  
      <div class="content">  
        <div ref="skillsSection" class="skills">  
          <h2>技能展示</h2>  
          <p>技能详细内容...</p>  
        </div>  
      </div>  
    </div>  
  </template>  
  
  <script setup lang="ts">  
  import { ref } from 'vue';  
  
  const skillsSection = ref<HTMLElement | null>(null);  
  
  const scrollToSkills = () => {  
    skillsSection.value?.scrollIntoView({ behavior: 'smooth' });  
  };  
  </script>  
  
  <style scoped>  
  .scroll-demo {  
    text-align: center;  
    margin-top: 20px;  
  }  
  .skills {  
    margin-top: 1000px;  
    padding: 20px;  
    background-color: #f1f1f1;  
    border-radius: 8px;  
  }  
  button {  
    background-color: #4caf50;  
    color: white;  
    padding: 10px 20px;  
    border: none;  
    border-radius: 5px;  
    cursor: pointer;  
  }  
  button:hover {  
    background-color: #388e3c;  
  }  
  </style> -->
  <template>  
    <div class="scroll-demo">  
      <button @click="scrollToSkills">滚动到技能展示</button>  
      <div class="content">  
        <div ref="skillsSection" class="skills">  
          <h2>技能展示</h2>  
          <p>技能详细内容...</p>  
        </div>  
      </div>  
  
      <button @click="scrollToTop" class="back-to-top">回到顶部</button>  
    </div>  
  </template>  
  
  <script setup lang="ts">  
  import { ref } from 'vue';  
  
  const skillsSection = ref<HTMLElement | null>(null);  
  
  const scrollToSkills = () => {  
    skillsSection.value?.scrollIntoView({ behavior: 'smooth' });  
  };  
  
  const scrollToTop = () => {  
    window.scrollTo({ top: 0, behavior: 'smooth' });  
  };  
  </script>  
  
  <style scoped>  
  .scroll-demo {  
    text-align: center;  
    margin-top: 20px;  
  }  
  .skills {  
    margin-top: 1000px;  
    padding: 20px;  
    background-color: #f1f1f1;  
    border-radius: 8px;  
  }  
  button {  
    background-color: #4caf50;  
    color: white;  
    padding: 10px 20px;  
    border: none;  
    border-radius: 5px;  
    cursor: pointer;  
    margin-top: 15px;  
  }  
  button:hover {  
    background-color: #388e3c;  
  }  
  .back-to-top {  
    position: fixed;  
    bottom: 20px;  
    right: 20px;  
    background-color: #2196F3;  
  }  
  .back-to-top:hover {  
    background-color: #1976D2;  
  }  
  </style>