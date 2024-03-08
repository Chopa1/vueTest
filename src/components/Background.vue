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
        </div>
        <div class="content">
            <div class="themes">
                <div class="PreviewAndBar">
                    <Preview />
                    <Bar />
                </div>
                <Theme themeName="Общее" :all = "true"/>
                <Theme themeName="Модуль 1. Объекты интеллектуальной собственности. Интеллектуальные права. Правовая охрана объектов интеллектуальной собственности" :all = "false"/>
                <Theme2 themeName="Модуль 2. Объекты интеллектуальной собственности. Интеллектуальные права." :all = "false"/>
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
        font-size: 0.83vw;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: center;

    }

    .PreviewAndBar{
        display: flex;
        flex-direction: column;
        gap: 20px;
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
        height: 60px;
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        top: 6px;
    }

    .content {
        display: flex;
        width: 100%;
        position: absolute;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        top: 128px;
    }

    .PurpleBackground{
        z-index: -2;
        width: 100%;
        display: flex;
        position: fixed;
    }

    img {
        display: flex;
        width: 100%;
    }

    .themes {
        display: flex;
        position: relative;
        flex-direction: column;
        top: -42px;
        gap: 25px;
        width: 69.5%;
        z-index: 2;
    }

    @media (max-width: 1200px) {
        .themes {
            width: 85%;
        }

        .GradBack {
            width: 95% !important;
        }

        .TextEnd {
            font-size: 16px !important;
        }
    }

    .GradBack {
        display: flex;
        position: fixed;
        margin-top: 183px;
        width: 82.4%;
        height: 100%;
        background: rgba(245, 245, 245, 1);
        border-radius: 24px 24px 0px 0px;
        justify-content: center;
        z-index: -1;
        flex-direction: column;
        align-items: center;
    }
</style>
