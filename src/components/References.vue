<script setup>
    import IconReference from './icons/IconReference.vue';
</script>

<template>
    <div class="reference">
        <div class="task">
            <IconReference />
            <h4 class="NameTask">Список литературы по модулю</h4>
        </div>
        <div class="conditions">
            <span class="ConText1">Надо сделать:</span>
            <span class="ConText2">Получить оценку</span>
        </div>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .reference {
        display: flex;
        padding: 5px 40px 13px 16px;
        align-items: center;
        gap: 5px;
    }

    .conditions {
        display: flex;
        flex-direction: row;
        background: rgba(188, 223, 255, 0.5);
        padding: 4px 8.5px 3px 8.5px;
        border-radius: 15px;
    }
    .ConText1 {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 9.7px;
        font-weight: 500;
        line-height: 15px;
        letter-spacing: 0em;
        text-align: left;

    }

    .ConText2 {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 9.5px;
        font-weight: 400;
        line-height: 15px;
        letter-spacing: 0em;
        text-align: left;
        padding-left: 4.5px;
        color: rgba(70, 73, 94, 1);

    }

    .task {
        display: flex;
        align-items: center;
        gap: 5px;
        width: 100%;
    }

    .NameTask {
        display: flex;
        margin: 0;
        font-family: "Montserrat", sans-serif;
        color: rgba(46, 49, 70, 1);
        text-align: center;
        font-size: 12.7px;
        font-weight: 500;
        line-height: 27px;
        letter-spacing: 0em;
        text-align: left;
        padding: 2px 0px 0px 10px;
    }
</style>