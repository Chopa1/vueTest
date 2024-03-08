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
        font-size: 24px;
        font-weight: 600;
        line-height: 30px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(46, 49, 70, 1);
        align-items: center;
    }

    @media (max-width: 1200px) {
        .percent {
            padding-right: 20px !important;
        }
    }

    .bar2 {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .bar {
        background: rgba(255, 255, 255, 1);
        box-shadow: 0px 0px 30px -10px rgba(70, 73, 94, 0.15);
        padding: 20px 40px 20px 40px;
        border-radius: 8px;
        gap: 30px;
        margin: 0px;
        display: flex;
        flex-direction: row;
        align-items: center;
    }

</style>