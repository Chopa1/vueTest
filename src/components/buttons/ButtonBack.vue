<script setup>
    import IconArrowBack from '../icons/IconArrowBack.vue'
</script>

<template>
    <div id="ButtonBack">
        <button class="buttonBack">
            <IconArrowBack />
            <span class="TextButton">Назад к списку курсов</span>
        </button>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

    #ButtonBack {
        display: flex;
        align-items: center;
        width: 100%;
        max-height: 44px;
        padding: 0px 30px 0px 30px;
        gap: 10px;
    }

    .buttonBack {
        display: flex;
        align-items: center;
        width: 100%;
        height: 100%;
        padding: 10px 26px;
        border-radius: 6px;
        border: 1px solid rgba(218, 221, 229, 1);
        gap: 20px;
        background: none;
    }

    .TextButton {
        display: flex;
        align-items: center;
        font-family: "Montserrat", sans-serif;
        max-height: 18px;
        font-size: 0.78125vw;
        font-weight: 400;
        line-height: 18px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(46, 49, 70, 1);
    }   

</style>