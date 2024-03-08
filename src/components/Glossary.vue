<script setup>
    import IconGlossary from './icons/IconGlossary.vue';
</script>

<template>
    <div class="reference">
        <div class="task">
            <IconGlossary />
            <h4 class="NameTask">Глоссарий</h4>
        </div>
        <button class="done">
            <span class="ConText2">Отметить как выполненный</span>
        </button>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .reference {
        display: flex;
        padding: 10px 20px 10px 19px;
        border-radius: 5px;
        gap: 5px;
        align-items: center;
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
    }

    .done {
        display: flex;
        padding: 7px 15px 7px 15px;
        border-radius: 6px;
        gap: 5px;
        border: 1px solid rgba(218, 221, 229, 1);
        background: rgba(255, 255, 255, 1);
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
        gap: 20px;
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
        padding-top: 1px;
    }
</style>