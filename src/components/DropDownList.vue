<script setup>
  import IconSidebar from './icons/IconSidebar.vue';
  import IconCircle from './icons/IconCircle.vue';
</script>

<template>
    <div class="dropdown2">
        <button class="dropdown-toggle" @click="toggleDropdown">
          <span class="title">{{ title }}</span>
          <i :class="{'arrow-right2': !isOpen, 'arrow-down2': isOpen}"></i>
        </button>
      <div class="dropdown-menu" :class="{ 'show': isOpen }">
        <a class="dropdown-item" href="#">
          <IconSidebar />
          <span class="dropdown-itemText">Задание</span>
          <div class="circle">
            <IconCircle />
          </div>
        </a>
        <a class="dropdown-item" href="#">
          <IconSidebar />
          <span class="dropdown-itemText">Лекция</span>
          <div class="circle">
            <IconCircle />
          </div>
        </a>
        <a class="dropdown-item" href="#">
          <IconSidebar />
          <span class="dropdown-itemText">Тест</span>
          <div class="circle">
            <IconCircle />
          </div>
        </a>
        <a class="dropdown-item" href="#">
          <IconSidebar />
          <span class="dropdown-itemText">Форум</span>
          <div class="circle">
            <IconCircle />
          </div>
        </a>
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
      padding: 15.5px 0px 10.5px 59px;
    }

    .title {
      width: 155px;
    }

    .arrow-right2 {
        border: solid #71809B;
        border-width: 0 2px 2px 0;
        padding: 2.5px;
        transform: rotate(-45deg);
        transition: transform 0.3s ease;
    }

    i {
        display: flex;
        position: absolute;
        right: -21px;
        top: 5px;
    }
    
    .arrow-down2 {
        border: solid #71809B;
        border-width: 0 2px 2px 0;
        padding: 2.5px;
        transform: rotate(45deg);
        transition: transform 0.3s ease;
    }
    
    .dropdown-toggle {
        cursor: pointer;
        border: 0;
        padding: 0;
        background-color: #EEF3FA;
        display: flex;
        font-family: "Montserrat", sans-serif;
        font-size: 11px;
        font-weight: 400;
        line-height: 18px;
        letter-spacing: 0em;
        text-align: left;
        color: #2E3146;
        position: relative;
        margin-bottom: 10px;
    }
    
    .dropdown-menu {
        display: none;
        bottom: 0;
    }

    .dropdown-itemText {
      display: flex;
      font-family: "Montserrat", sans-serif;
      font-size: 11px;
      color: #2E3146;
      font-weight: 400;
      line-height: 18px;
      letter-spacing: 0em;
      padding-left: 15px;
    }
    
    .dropdown-menu.show {
        display: flex;
        flex-direction: column;
        gap: 3px;
        padding-right: 24px;
    }
    
    .dropdown-item {
        color: #212529;
        padding: 5px 0px 5px 16px;
        text-decoration: none;
        display: flex;
        border-radius: 6px;
        align-items: center;
        position: relative;
    }

    .circle {
      display: flex;
      position: absolute;
      right: 12.5px;
      top: 10.5px;
    }
    
    .dropdown-item:hover {
        background-color: #E0E8F4;
    }
  </style>
  