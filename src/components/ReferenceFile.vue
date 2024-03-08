<script setup>
    import IconFile from './icons/IconFile.vue';
    import IconCheck2 from './icons/IconCheck2.vue';

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
                    <IconCheck2 />
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
        align-items: center;
        padding: 10px 20px 10px 20px;
        border-radius: 5px;
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

        .ConText2 {
            font-size: 14px !important;
        }

        .ConText2No {
            font-size: 14px !important;
        }
        
        .text1 {
            font-size: 10px !important;
        }
    }

    .done {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 100%;
        padding: 7px 20px 7px 15px;
        border-radius: 6px;
        gap: 5px;
        border: 1px solid rgba(172, 217, 193, 1);
        background: rgba(255, 255, 255, 1);
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
        color: rgba(14, 131, 69, 1);
        padding-right: 1px;
    }

    .doneNo {
        display: flex;
        padding: 7px 15px 7px 15px;
        border-radius: 6px;
        gap: 5px;
        border: 1px solid rgba(218, 221, 229, 1);
        background: none;
        margin: 0;
    }

    .ConText2No {
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
        padding-top: 2px;

    }
</style>