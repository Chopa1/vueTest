<script setup>
    import IconFile from './icons/IconFile.vue';
    import IconCheck from './icons/IconCheck.vue';

    const props = defineProps({
        themeBool: Boolean,
    });
</script>

<template>
    <div class="reference">
        <div class="task">
            <IconFile />
            <h4 class="NameTask">Список литературы по модулю</h4>
        </div>
        <div class="conditions">

            <template v-if="themeBool">
                <button class="done">
                    <IconCheck />
                    <span class="ConText2">Выполнено</span>
                </button>
            </template>

            <template v-else>
                <button class="doneNo">
                    <span class="ConText2No">Отметить как выполненный</span>
                </button>
            </template>
        </div>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .reference {
        display: flex;
        padding: 5px 40px 13px 15.5px;
        align-items: center;
        gap: 5px;
    }

    .done {
       display: flex;
       flex-direction: row;
       align-items: center;
       width: 100%;
       padding-left: 12px;
       padding-top: 3px;
       border-radius: 5px;
       padding-right: 15px;
       border: 1.5px solid rgba(172, 217, 193, 1);
       background: rgba(255, 255, 255, 1);
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
        padding-left: 3px;
        color: rgba(14, 131, 69, 1);

    }

    .doneNo {
       display: flex;
       width: 100%;
       padding-left: 12px;
       padding-top: 3px;
       border-radius: 5px;
       padding-right: 10px;
       border: 1.5px solid rgba(218, 221, 229, 1);
       background: rgba(255, 255, 255, 1);
    }

    .ConText2No {
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