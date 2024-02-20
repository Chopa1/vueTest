<script setup>
    import IconGlossary from './icons/IconGlossary.vue';
</script>

<template>
    <div class="reference">
        <div class="task">
            <IconGlossary />
            <h4 class="NameTask">Глоссарий</h4>
        </div>
        <div class="conditions">
            <button class="done">
                <span class="ConText2">Отметить как выполненный</span>
            </button>
        </div>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .reference {
        display: flex;
        padding: 5px 38px 13px 16px;
        align-items: center;
        gap: 5px;
    }

    .done {
       display: flex;
       width: 100%;
       padding-left: 11px;
       padding-top: 3px;
       border-radius: 5px;
       padding-right: 12px;
       border: 1.5px solid rgba(218, 221, 229, 1);
       background: rgba(255, 255, 255, 1);
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