<script setup>
    import IconBar from './icons/IconBar.vue';
</script>

<template>
    <div class="bar">
        <div class="bar2">
            <IconBar />
        </div>
        <span class="percent">71%</span>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

    .percent{
        display: flex;
        font-family: "Montserrat", sans-serif;
        font-size: 19px;
        font-weight: 600;
        line-height: 30px;
        letter-spacing: 0.03em;
        text-align: left;
        color: rgba(46, 49, 70, 1);
        align-items: center;
        padding-left: 54px;
    }

    .bar2 {
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        left: 31px;
    }

    .bar {
        background: rgba(255, 255, 255, 1);
        box-shadow: 0px 0px 30px -10px rgba(70, 73, 94, 0.15);
        border-radius: 9px;
        width: 100%;
        height: 7px;
        margin: 0px;
        display: flex;
        padding: 24px 0px 24px 0px;
        flex-direction: row;
    }

</style>