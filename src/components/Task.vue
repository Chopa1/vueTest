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
        padding: 10px 20px 10px 20px;
        border-radius: 5px;
        justify-content: space-between;
        align-items: start;
    }

    @media (max-width: 1200px) {
        .reference {
            flex-direction: column;
        }
        
        .group1 {
            justify-content: center !important;
            align-items: center !important;
        }

        .NameTask {
            font-size: 12px !important;
            width: 150px !important;
        }

        .ConText1, .ConText2, .ConText3, .ConText4 {
            font-size: 12px !important;
        }
    }

    .group1 {
        display: flex;
        flex-direction: column;
        gap: 6.5px;
        justify-content: flex-end;
        align-items: flex-end;
    }

    .conditions {
        display: flex;
        flex-direction: row;
        background: rgba(188, 223, 255, 0.5);
        padding: 5px 13px 5px 12px;
        border-radius: 15px;
        gap: 5px;
    }

    .ConText1 {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 0.625vw;
        font-weight: 500;
        line-height: 15px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(70, 73, 94, 1);
    }

    .ConText2 {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 0.625vw;
        font-weight: 400;
        line-height: 15px;
        letter-spacing: 0em;
        padding-left: 2px;
        text-align: left;
        color: rgba(70, 73, 94, 1);
    }

    .conditions2 {
        display: flex;
        flex-direction: row;
        background: rgba(231, 243, 233, 1);
        padding: 5px 14px 5px 12px;
        border-radius: 15px;
        gap: 2px;
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

    .ConText4 {
        font-size: 0.625vw;
        font-weight: 500;
        line-height: 15px;
        letter-spacing: 0em;
        text-align: left;
    }

    .ConText3 {
        font-size: 0.625vw;
        font-weight: 400;
        line-height: 15px;
        letter-spacing: 0em;
        text-align: left;
    }

    .task {
        display: flex;
        align-items: center;
        gap: 19px;
        width: 100%;
    }

    .NameTask {
        display: flex;
        margin: 0;
        font-family: "Montserrat", sans-serif;
        color: rgba(46, 49, 70, 1);
        text-align: center;
        font-size: 0.83vw;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
    }
</style>