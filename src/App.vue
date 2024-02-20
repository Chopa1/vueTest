<template>
  <div class="all">
    <header>
      <div class="wrapper">
        <!-- При ширине меньше 1200px показывается кнопка для открытия Header1 -->
        <!-- <button v-if="windowWidth < 1200" @click="toggleHeader" class="open-header-btn">Open Header1</button> -->
        <Header1 v-if="windowWidth >= 1200" />
      </div>
    </header>

    <aside>
      <ButtonBack v-if="windowWidth >= 1200"/>
      <Sidebar v-if="windowWidth >= 1200"/>
      <AdditionalInformation v-if="windowWidth >= 1200"/>
    </aside>

    <main>
      <Background />
    </main>
  </div>
</template>

<script setup>
  import { ref, onMounted, onUnmounted } from 'vue'; // Используем Vue 3
  import Header1 from './components/Header.vue'
  import Sidebar from './components/Sidebar.vue'
  import ButtonBack from './components/buttons/ButtonBack.vue'
  import AdditionalInformation from './components/AdditionalInformation.vue';
  import Background from './components/Background.vue';

  const windowWidth = ref(window.innerWidth);
</script>

<style scoped>
  /* Стили остаются без изменений */
</style>


<style scoped>

  @import url("https://fonts.googleapis.com/css2?family=Lato:wght@300&display=swap");

  header {
    display: flex;
    width: 100%;
    grid-area: header;
  }

  .all {
    width: 100%;
    display: grid;
    grid-template-columns: 265px 82.5%;
    grid-template-areas: 'header header' 'sidebar content';
  }

  @media (max-width: 1200px) {
    .all {
      grid-template-areas: 'header header' 'content content';
    }
  }

  .wrapper{
    display: flex;
    width: 100%;
  }

  aside {
    display: flex;
    flex-wrap: wrap;
    grid-area: sidebar;
    background: #FFFFFF;
    padding: 24px 0px 39px 0px;
    gap: 20px;
  }

  main {
    grid-area: content;
    height: fit-content;
  }
</style>
