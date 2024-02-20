<template>
    <div class="full">
      <div class="dropdown" @click="toggleDropdown">
        <div class="IconContentAndContent">
          <IconContent />
          <span class="content">Содержание</span>
        </div>
        <i :class="{'arrow-right': !showContent, 'arrow-down': showContent}"></i>
      </div>
      <div v-if="showContent" class="content-dropdown">
        <DropDownList title="Тема 1. Основы технологии производства ЭС" />
        <DropDownList title="Тема 2. Моделирование бизнес-процессов предметной области" />
        <DropDownList title="Тема 3. Модели разработки программного продукта" />
      </div>
    </div>
</template>
  
<script setup>
    import IconContent from './icons/IconContent.vue';
    import DropDownList from './DropDownList.vue';
    import { ref } from 'vue';
    
    const showContent = ref(true);
    
    const toggleDropdown = () => {
        showContent.value = !showContent.value;
    };
</script>
  
<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .dropdown {
        width: 100%;
        cursor: pointer;
        display: flex;
        align-items: center;
        position: relative;
        margin: 0 20px 0px 25px;
    }

    i {
        display: flex;
        position: absolute;
        right: 9px;
        align-items: center;
        bottom: 8px;
    }

    .content {
      display: flex;
      align-items: center;
      font-family: "Montserrat", sans-serif;
      font-size: 11px;
      font-weight: 400;
      line-height: 18px;
      letter-spacing: 0em;
      color: #2E3146;
    }

    .IconContentAndContent{
      display: flex;
      gap: 16px;
    }

    .full {
        width: 100%;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        position: relative;
        top: 4px;
    }
    
    .arrow-right {
        border: solid #71809B;
        border-width: 0 2px 2px 0;
        padding: 3px;
        transform: rotate(-45deg);
        transition: transform 0.3s ease;
    }
    
    .arrow-down {
        border: solid #71809B;
        border-width: 0 2px 2px 0;
        padding: 3px;
        transform: rotate(45deg);
        transition: transform 0.3s ease;
    }
    
    .content-dropdown {
      margin-top: 16px;
      width: 100%;
      border-radius: 8px;
      background-color: #EEF3FA;
    }
</style>
  