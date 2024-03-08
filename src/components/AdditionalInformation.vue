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
        gap: 20px;
    }

    .AddinInform{
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 0px 30px 0px 30px;
        gap: 20px;
    }

    .TextAddin {
        display: flex;
        align-items: center;
        font-family: "Montserrat", sans-serif;
        font-size: 0.72916vw;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
    }

    @media (max-width: 1200px) {
        .TextAddin {
            font-size: 14px;
        }
    }

</style>