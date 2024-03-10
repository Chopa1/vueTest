<script setup>
    import IconFolder from './icons/IconFolder.vue';
    import IconLock from './icons/IconLock.vue'
</script>

<template>
    <div class="fullRef">
        <div class="reference">
            <div class="task">
                <IconFolder />
                <h4 class="NameTask">Список литературы по модулю</h4>
            </div>
            <button class="done">
                <span class="ConText2">Отметить как выполненный</span>
            </button>
        </div>
        <div class="info">
            <IconLock />
            <div class="fullText">
                <span class="text1">Недоступно, пока не выполнено: Элемент курса</span>
                <span class="text1">Задание должен быть отмечен как выполненный</span>
            </div>
        </div>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .fullRef {
        display: flex;
        align-items: flex-start;
        flex-direction: column;
        background: rgba(233, 242, 255, 0.4);
        padding: 9px 20px 10px 20px;
        border-radius: 5px;
        gap: 6px;

    }

    @media (max-width: 1200px) {
        .reference {
            flex-direction: column;
        }

        .NameTask {
            font-size: 12px !important;
            width: 150px !important;
        }

        .ConText2 {
            font-size: 14px !important;
        }
        
        .text1 {
            font-size: 12px !important;
        }

        .fullText {
            width: 150px !important;
        }
    }

    .fullText {
        display: flex;
        flex-direction: column;
    }

    .text1 {
        font-family: "Montserrat", sans-serif;
        font-size: 0.625vw;
        font-weight: 400;
        line-height: 19px;
        letter-spacing: 0em;
        text-align: left;
    }

    .reference {
        display: flex;
        gap: 5px;
        align-items: center;
        width: 100%;
        padding-bottom: 6px;
    }

    .info {
        display: flex;
        flex-direction: row;
        background: rgba(233, 242, 255, 0.6);
        width: 97.5%;
        padding: 7px 11px;
        border-radius: 5px;
        gap: 10px;
        align-items: center;
    }

    .done {
        display: flex;
        padding: 7px 15px 7px 15px;
        border-radius: 6px;
        gap: 5px;
        border: 1px solid rgba(218, 221, 229, 1);
        background: none;
        margin: 0;
    }

    .ConText2 {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 0.72916vw;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(70, 73, 94, 1);
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
        font-size: 0.83vw;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
        padding-top: 3px;
    }
</style>