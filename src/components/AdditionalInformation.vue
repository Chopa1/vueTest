<script setup>
    import IconEvaluations from './icons/IconEvaluations.vue';
    import IconParticipants from './icons/IconParticipants.vue';
</script>

<template>
    <div class="AddinInform">
        <a class="participants" href="#">
            <IconParticipants />
            <span class="TextAddin">Участники</span>
        </a>
        <a class="evaluations" href="#">
            <IconEvaluations />
            <span class="TextAddin">Оценки</span>
        </a>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .participants, .evaluations {
        display: flex;
        flex-direction: row;
        align-items: center;
        text-decoration: none;
    }

    .AddinInform{
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 0px 20px 0px 23px;
        gap: 16px;
    }

    .TextAddin {
        display: flex;
        align-items: center;
        font-family: "Montserrat", sans-serif;
        font-size: 11px;
        font-weight: 400;
        line-height: 18px;
        letter-spacing: 0em;
        color: #2E3146;
        padding-left: 17px;
        padding-top: 1px;
    }
</style>