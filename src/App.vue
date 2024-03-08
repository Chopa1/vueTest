<template>
  <div class="all">
    <header>
      <div class="wrapper">
        <Header1 />
      </div>
    </header>

    <button @click="toggleSidebar" class="toggle-btn" v-if="windowWidth <= 1200">☰</button>

    <aside :class="{ 'show-sidebar': showSidebar }">
      <ButtonBack v-if="windowWidth >= 1200"/>
      <Sidebar />
      <AdditionalInformation/>
      <button v-if="windowWidth <= 1200" @click="toggleSidebar" class="close-btn">✕</button>
    </aside>

    <main :class="{ 'blur-background': showSidebar }">
      <Background />
    </main>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  import Header1 from './components/Header.vue';
  import Sidebar from './components/Sidebar.vue';
  import ButtonBack from './components/buttons/ButtonBack.vue';
  import AdditionalInformation from './components/AdditionalInformation.vue';
  import Background from './components/Background.vue';

  const windowWidth = ref(window.innerWidth);

  const showSidebar = ref(false);

  const toggleSidebar = () => {
    showSidebar.value = !showSidebar.value;
  };
</script>


<style scoped>

  @import url("https://fonts.googleapis.com/css2?family=Lato:wght@300&display=swap");

  header {
    display: flex;
    width: 100%;
    grid-area: header;
    position: fixed;
    background: #FFFFFF;
    z-index: 30;
  }

  .all {
    width: 100%;
    display: grid;
    grid-template-columns: 17.5% 82.5%;
    grid-template-areas: 'header header' 'sidebar content';
  }

  @media (max-width: 1200px) {
    .all {
      grid-template-areas: 'header header' 'content content';
      grid-template-columns: 100%;
    }

    .toggle-btn {
      position: fixed;
      left: -5px;
      top: 100px;
      background: rgb(255, 255, 255);
      border-radius: 5px 35px 35px 5px;
      width: 40px;
      height: 60px;
      z-index: 3;
      border: 1px solid rgb(169, 169, 169);
    }

    .show-sidebar {
      transform: translateX(0%);
    }

    .close-btn {
      position: absolute;
      top: 0px;
      right: 0px;
      font-size: 15px;
      font-weight: 700;
      background: transparent;
      border: none;
      cursor: pointer;
    }

    .blur-background {
      filter: blur(5px);
    }

    aside {
      transform: translateX(-600%);
      transition: transform 0.3s ease;
      z-index: 10;
      width: 260px !important;
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
    background: rgba(255, 255, 255, 1);
    padding: 30px 0px 39px 0px;
    margin-top: 75px;
    position: fixed;
    width: 17.5%;
    max-height: calc(100vh - 150px);
    overflow-y: auto;
  }

  main {
    grid-area: content;
    height: fit-content;
    margin-top: 59px;
  }
</style>
