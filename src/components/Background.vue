<script setup>
    import Preview from './Preview.vue';
    import Bar from './Bar.vue';
    import Theme from './Theme.vue';
    import Theme2 from './Theme2.vue';
</script>

<template>
    <div class="background">
        <div class="PurpleBackground">
            <img src="/Монтажная область 1@4x 1.png" height="200px">
        </div>
        <div class="GradBack">
            <div class="themes">
                <div class="PreviewAndBar">
                    <Preview />
                    <Bar />
                </div>
                <div class="themes1">
                    <Theme themeName="Общее" :all = "true"/>
                    <Theme themeName="Модуль 1. Объекты интеллектуальной собственности. Интеллектуальные права. Правовая охрана объектов интеллектуальной собственности" :all = "false"/>
                    <Theme2 themeName="Модуль 2. Объекты интеллектуальной собственности. Интеллектуальные права." :all = "false"/>
                </div>
            </div>
            <div class="end">
                <p class="TextEnd">ДПО СибГМУ</p>
            </div>
        </div>
    </div>
</template>

<style scoped>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    .TextEnd {
        color: rgba(113, 128, 155, 1);
        font-family: "Montserrat", sans-serif;
        font-size: 12.5px;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: center;
        padding-left: 4px;

    }

    @media (max-width: 1200px) {
        .background {
            width: 1200px !important;
        }
    }

    @media (max-width: 800px) {
        .background {
            width: 1000px !important;
        }
    }

    .PreviewAndBar{
        display: flex;
        flex-direction: column;
        gap: 17px;
    }
    .background {
        display: flex;
        width: 100%;
        position: relative;
        align-items: center;
        flex-direction: column;
    }

    .end {
        width: 100%;
        background: #FFFFFF;
        border-top: 1px solid rgba(218, 221, 229, 1);
        height: 46px;
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        bottom: -6.7px;
    }

    .themes1 {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .PurpleBackground{
        z-index: 0;
        width: 100%;
        display: flex;
    }

    img {
        display: flex;
        width: 100%;
    }

    .themes {
        display: flex;
        position: relative;
        flex-direction: column;
        top: -77px;
        gap: 19px;
        width: 870px;
    }
    .GradBack {
        display: flex;
        position: absolute;
        top: 132px;
        width: 100%;
        height: fit-content;
        background: rgba(245, 245, 245, 1);
        border-radius: 20px 20px 0px 0px;
        justify-content: center;
        z-index: 0;
        flex-direction: column;
        align-items: center;
    }
</style>
