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
      <div class="icons">
        <div class="notification">
          <div class="icon">
            <IconNotification />
          </div>
        </div>
        <div class="message">
          <div class="icon">
            <IconMessage />
          </div>
        </div>
        <div class="calendar">
          <div class="icon">
            <IconCalendar />
          </div>
        </div>
      </div>
    </div>
    <div class="profile" >
      <div class="fio">
        <img src="/фото студента.png" width="28px" height="29px">
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
  height: 58px;
  width: 100%;
  align-items: center;
}

@media (max-width: 1200px) {
  .logo {
    width: 200px !important;
  }

  .profile {
    position: absolute;
    right: 0px !important;
  }

  .head {
    position: relative !important;
  }
}

.profile {
  display: flex;
  align-items: center;
  right: 0px;
  height: 58px;
  position: absolute;
}

.exit {
  display: flex;
  align-items: center;
  width: 97px;
  height: 50px;
}

.TextExit{
  font-family: "Montserrat", sans-serif;
  font-size: 11px;
  font-weight: 400;
  line-height: 17px;
  letter-spacing: 0em;
  text-align: center;
  width: auto;
  color: #71809B;
}

.exit .TextExit {
  position: relative;
  left: 26px;
}

.fio {
  display: flex;
  gap: 17px;
  align-items: center;
  height: 30px;
  padding: 0 21px 0px 10px;
  border-right: 1px solid #DADDE5;
}

.IconsLogo{
  display: flex;
  justify-content: start;
  height: 100%;
  align-items: center;
}

.icons {
  display: flex;
  height: 100%;
  align-items: center;
}

.notification, .message, .calendar {
  display: flex;
  align-items: center;
  height: 100%;
  width: 68px;
  justify-content: center;
}

.icon {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 25px;
  height: 25px;
}

.logo{
  display: flex;
  width: 265px;
  height: 23px;
  padding: 5px 0px;
  border-right: 1px solid #DADDE5;
  justify-content: center;
  flex-wrap: wrap;
  align-content: center;
}
</style>
