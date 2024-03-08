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
        padding: 9px 20px 10px 19px;
        border-radius: 5px;
        gap: 5px;
        align-items: center;
        gap: 5px;
    }

    @media (max-width: 1200px) {
        .reference {
            flex-direction: column;
        }

        .NameTask {
            font-size: 12px !important;
            width: 150px !important;
        }

        .ConText1, .ConText2 {
            font-size: 12px !important;
        }
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

    .task {
        display: flex;
        align-items: center;
        gap: 20px;
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