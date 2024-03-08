<script setup>
  import IconSidebar from './icons/IconSidebar.vue';
  import IconCircle from './icons/IconCircle.vue';
  import IconArrow from './icons/IconArrow.vue';
</script>

<template>
    <div class="dropdown2">
      <div class="dropdown3">
        <div class="dropdown-toggle" @click="toggleDropdown">
          <span class="title">{{ title }}</span>
          <div :class="{'arrow-right2': !isOpen, 'arrow-down2': isOpen}">
            <IconArrow />
          </div>
      </div>
      <div class="dropdown-menu" :class="{ 'show': isOpen }">
        <a class="dropdown-item" href="#">
          <div class="IconAndTitle">
            <IconSidebar />
            <span class="title">Задание</span>
          </div>
          <IconCircle />
        </a>
        <a class="dropdown-item" href="#">
          <div class="IconAndTitle">
            <IconSidebar />
            <span class="title">Лекция</span>
          </div>
          <IconCircle />
        </a>
        <a class="dropdown-item" href="#">
          <div class="IconAndTitle">
            <IconSidebar />
            <span class="title">Тест</span>
          </div>
          <IconCircle />
        </a>
        <a class="dropdown-item" href="#">
          <div class="IconAndTitle">
            <IconSidebar />
            <span class="title">Форум</span>
          </div>
          <IconCircle />
        </a>
      </div>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: true
      }
    },
    data() {
      return {
        isOpen: true
      };
    },
    methods: {
      toggleDropdown() {
        this.isOpen = !this.isOpen;
      }
    }
  };
  </script>
  
  <style scoped>

    @import url("https://fonts.googleapis.com/css2?family=Lato:wght@300&display=swap");
    .dropdown2 {
      height: fit-content;
      padding: 19px 30px 18px 74px;
      border-radius: 8px;
    }

    .dropdown3 {
      display: flex;
      flex-direction: column;
      height: fit-content;
      gap: 15.5px;
    }

    .title {
      height: 100%;
      font-family: "Montserrat", sans-serif;
      font-size: 0.72916vw;
      font-weight: 400;
      line-height: 22px;
      letter-spacing: 0em;
      text-align: left;
      color: rgba(46, 49, 70, 1);
    }

    @media (max-width: 1200px) {
      .title {
        font-size: 14px;
      }
    }

    .arrow-right2 {
      transform: rotate(-90deg);
      transition: transform 0.3s ease;
      height: fit-content;
    }

    .IconAndTitle {
      max-width: 177px;
      max-height: 22px;
      gap: 20px;
      display: flex;
    }
    
    .arrow-down2 {
      transform: rotate(0deg);
      transition: transform 0.3s ease;
      height: fit-content;
    }
    
    .dropdown-toggle {
      cursor: pointer;
      display: flex;
      width: 100%;
      height: fit-content;
      gap: 10px
    }
    
    .dropdown-menu {
      display: none;
    }

    .dropdown-itemText {
      display: flex;
      font-family: "Montserrat", sans-serif;
      font-size: 10.9px;
      color: #2E3146;
      font-weight: 400;
      line-height: 18px;
      letter-spacing: 0em;
      padding-left: 15px;
    }
    
    .dropdown-menu.show {
        display: flex;
        flex-direction: column;
        width: 100%;
        height: fit-content;
        gap: 7px
    }
    
    .dropdown-item {
      text-decoration: none;
      display: flex;
      align-items: center;
      position: relative;
      max-height: 34px;
      padding: 5px 10px 5px 20px;
      border-radius: 6px;
      justify-content: space-between;
    }
    
    .dropdown-item:hover {
        background-color: rgba(224, 232, 244, 1);
;
    }
  </style>
  