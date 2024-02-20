<script setup>
    import IconCheck from './icons/IconCheck.vue';
    import IconTask from './icons/IconTask.vue';
</script>

<template>
    <div class="reference">
        <div class="task">
            <IconTask />
            <h4 class="NameTask">Задание</h4>
        </div>
        <div class="group1">
            <div class="conditions">
                <span class="ConText1">Надо сделать:</span>
                <span class="ConText2">Получить оценку</span>
            </div>
            <div class="conditions2">
                <IconCheck />
                <span class="ConText4">Выполнено:</span>
                <span class="ConText3">Просмотреть</span>
            </div>
            <div class="conditions2">
                <IconCheck />
                <span class="ConText4">Выполнено:</span>
                <span class="ConText3">Получить оценку</span>
            </div>
        </div>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .reference {
        display: flex;
        padding: 5px 40px 13px 15.5px;
        align-items: start;
        gap: 5px;
    }

    .group1 {
        display: flex;
        flex-direction: column;
        gap: 5px;
        justify-content: flex-end;
        align-items: flex-end;
    }

    .conditions {
        display: flex;
        flex-direction: row;
        background: rgba(188, 223, 255, 0.5);
        padding: 5px 8.5px 4px 8.5px;
        border-radius: 15px;
    }

    .conditions2 {
        display: flex;
        flex-direction: row;
        background: rgba(231, 243, 233, 1);
        padding: 1.5px 8px 1.5px 8px;
        border-radius: 15px;
        width: fit-content;
    }

    .conditions2> * {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        line-height: 15px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(14, 131, 33, 1);
    }

    .conditions span {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        line-height: 15px;
        letter-spacing: 0em;
        text-align: left;
    }

    .ConText1 {
        font-size: 9.7px;
        font-weight: 500;
    }

    .ConText4 {
        font-size: 9.7px;
        font-weight: 500;
;
    }

    .ConText2 {
        font-size: 9.5px;
        font-weight: 400;
        padding-left: 4.5px;

    }

    .ConText3 {
        font-size: 9.5px;
        font-weight: 400;
        padding-left: 2.2px;
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