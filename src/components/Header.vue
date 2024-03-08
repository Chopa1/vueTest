<script setup>
  import { ref } from 'vue'; // Используем Vue 3
  import IconTusur from './icons/IconTusur.vue';
  import IconNotification from './icons/IconNotification.vue'
  import IconMessage from './icons/IconMessage.vue'
  import IconCalendar from './icons/IconCalendar.vue'
  const windowWidth = ref(window.innerWidth);
</script>

<template>
  <div class="head">
    <div class="IconsLogo">
      <div class="logo">
        <IconTusur />
      </div>
      <div class="icons" v-if="windowWidth >= 1200">
        <div class="icon">
          <IconNotification />
        </div>
        <div class="icon">
          <IconMessage />
        </div>
        <div class="icon">
          <IconCalendar />
        </div>
      </div>
    </div>
    <div class="profile">
      <div class="fio">
        <img src="/фото студента.png">
        <span class="TextExit">Иван Иванов</span>
      </div>
      <div class="exit">
        <span class="TextExit">Выход</span>
      </div>
    </div>
  </div>
</template>

<style scoped>

@import url("https://fonts.googleapis.com/css2?family=Lato:wght@300&display=swap");
.head {
  display: flex;
  border-bottom: 1px solid #DADDE5;
  box-shadow: 0px 1px 0px 0px #DADDE566;
  height: 75px;
  width: 100%;
  align-items: center;
}

@media (max-width: 1200px) {
  .logo {
    width: 150px !important;
    border-right: none !important;
  }

  .profile {
    position: absolute;
    right: 0px !important;
  }

  .head {
    position: relative !important;
  }

  .exit {
    padding: 0px 10px 0px 10px !important;
  }

  .fio {
    padding: 0px 10px 0px 10px !important;
  }

  .TextExit {
    font-size: 12px !important;
  }
}

.profile {
  display: flex;
  align-items: center;
  right: 0px;
  height: 100%;
  position: absolute;
}

.exit {
  display: flex;
  max-height: 50px;
  padding: 10px 45px 10px 30px;
  gap: 10px;
}

.TextExit{
  display: flex;
  font-family: "Montserrat", sans-serif;
  font-size: 0.72916vw;
  font-weight: 400;
  line-height: 17px;
  letter-spacing: 0em;
  text-align: center;
  max-height: 17px;
  color: rgba(113, 128, 155, 1);
}

.fio {
  display: flex;
  height: 39px;
  padding: 0px 30px 0px 30px;
  border-right: 1px solid rgba(218, 221, 229, 1);
  gap: 20px;
  align-items: center;
}

.fio img {
  max-height: 35.5px;
}

.IconsLogo{
  display: flex;
  justify-content: start;
  max-height: 100%;
  align-items: center;
}

.icons {
  display: flex;
  height: 100%;
  align-items: center;
}

.icon {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 4.5072916vw;
  height: 100%;
}

.logo{
  display: flex;
  width: 17.447916vw;
  height: 38.56px;
  padding: 5px 0px;
  border-right: 1px solid #DADDE5;
  justify-content: center;
  flex-wrap: wrap;
  align-content: center;
}
</style>
