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
        padding: 0 20px 0px 23px;
    }

    .buttonBack {
        display: flex;
        align-items: center;
        background: #FFFFFF;
        border: 1px solid #DADDE5;
        border-radius: 6px;
        padding: 7px 20px 6px 21.6px;
    }

    .TextButton {
        display: flex;
        align-items: center;
        padding: 1px 0px 0px 14px;
        font-family: "Montserrat", sans-serif;
        font-size: 12px;
        font-weight: 400;
        line-height: 18px;
        letter-spacing: 0em;
        color: #2E3146;
    }

</style>