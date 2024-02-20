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
            <div class="conditions">
                <button class="done">
                    <span class="ConText2">Отметить как выполненный</span>
                </button>
            </div>
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
        padding: 7px 16px 14px 16px;
        align-items: flex-start;
        flex-direction: column;
        background: rgba(233, 242, 255, 0.4);
        border-radius: 5px;
        margin-right: 24px;
    }

    .fullText {
        display: flex;
        flex-direction: column;
        gap: 3px;
    }

    .text1 {
        font-family: "Montserrat", sans-serif;
        font-size: 9.5px;
        font-weight: 500;
        line-height: 11.5px;
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
        width: 100%;
        padding: 9.5px 0px 8px 9.6px;
        align-items: center;
        gap: 7.5px;
        border-radius: 5px;
    }

    .done {
       display: flex;
       width: 100%;
       padding-left: 11px;
       padding-top: 3px;
       border-radius: 5px;
       padding-right: 10px;
       border: 1.5px solid rgba(218, 221, 229, 1);
       background: none;
       margin: 0;
    }

    .ConText2 {
        display: flex;
        text-align: center;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 11px;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
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