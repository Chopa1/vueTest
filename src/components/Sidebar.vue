<template>
    <div class="full">
      <div class="dropdown" @click="toggleDropdown">
        <div class="IconContentAndContent">
          <IconContent />
          <span class="content">Содержание</span>
        </div>
        <div :class="{'arrow-right': !showContent, 'arrow-down': showContent}">
          <IconArrow />
        </div>
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
    import IconArrow from './icons/IconArrow.vue';
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
      max-height: 24px;
      padding: 0px 30px 0px 30px;
      justify-content: space-between;

    }

    .content {
      display: flex;
      align-items: center;
      font-family: "Montserrat", sans-serif;
      height: 100%;
      font-size: 0.72916vw;
      font-weight: 400;
      line-height: 22px;
      letter-spacing: 0em;
      text-align: left;
      color: rgba(46, 49, 70, 1);
    }

    @media (max-width: 1200px) {
      .content {
        font-size: 14px !important;
      }

      .full {
        padding-top: 0px !important;
      }
    }

    .IconContentAndContent{
      display: flex;
      width: 100%;
      max-width: 251px;
      max-height: 24px;
      gap: 20px;
    }

    .full {
      width: 100%;
      display: flex;
      height: fit-content;
      align-items: center;
      flex-wrap: wrap;
      position: relative;
      gap: 20px;
      padding: 30px 0px 18px 0px;
    }
    
    .arrow-right {
      margin-top: 2px;
      transform: rotate(-90deg);
      transition: transform 0.3s ease;
    }
    
    .arrow-down {
      margin-top: 2px;
      transform: rotate(0deg);
      transition: transform 0.3s ease;
    }
    
    .content-dropdown {
      width: 100%;
      height: fit-content;
      border-radius: 15px;
      background-color: rgba(236, 241, 248, 0.5);
    }
</style>
  