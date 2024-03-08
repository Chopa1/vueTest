<template>
    <div class="theme">
        <div class="name" @click="toggleDropdown">
            <div :class="{'BackArrow': !showContent, 'BackArrow-Down': showContent}">
                <IconArrowTheme />
            </div>
            <span class="content">{{ themeName }}</span>
            <div v-if="all && windowWidth >= 1200" class="all">
                <span class="allTheme">Свернуть всё</span>
            </div>
        </div>
        <div v-if="showContent" class="content-dropdown">
            <div class="title">
                <div class="text3">
                    <p class="text">Материалы для изучения</p>
                </div>
            </div>
            <References />
            <Glossary />
            <Task />
            <ReferenceFolder />
            <ReferenceFile :themeBool="true"/>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import IconArrowTheme from './icons/IconArrowTheme.vue';
    import References from './References.vue';
    import Glossary from './Glossary.vue';
    import Task from './Task.vue';
    import ReferenceFolder from './ReferenceFolder.vue';
    import ReferenceFile from './ReferenceFile.vue';

    import { defineProps } from 'vue';
    
    const showContent = ref(true);
    const windowWidth = ref(window.innerWidth);
    
    const toggleDropdown = () => {
        showContent.value = !showContent.value;
    };

    const props = defineProps({
        themeName: String,
        all: Boolean,
    });
</script>

<style scoped>

    @import url("https://fonts.googleapis.com/css2?family=Lato:wght@300&display=swap");
    .theme{
        background: rgba(255, 255, 255, 1);
        box-shadow: 0px 0px 40px 0px rgba(29, 38, 122, 0.05);
        display: flex;
        padding: 30px;
        border-radius: 8px;
        gap: 30px;
        flex-direction: column;
    }

    .all {
        display: flex;
        z-index: 1;
        position: relative;
        top: 1px;
        right: 1px;
    }

    .allTheme {
        display: flex;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 0.83vw;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: right;
        color: rgba(39, 55, 102, 1);
    }

    .title {
        display: flex;
        padding: 14px 20px 10px 20px;
    }

    .text {
        display: flex;
        font-family: "Montserrat", sans-serif;
        font-size: 0.83vw;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
        margin: 0;
        color: rgba(46, 49, 70, 1);
    }

    .text3 {
        display: flex;
        padding: 0px 20px 0px 0px;
        gap: 20px;
    }

    .name {
        display: flex;
        cursor: pointer;
        align-items: center;
        align-items: flex-start;
        padding: 0px 20px 0px 0px;
        gap: 14px;
    }

    @media (max-width: 1200px) {
        .name {
            width: 80%;
        }

        .content {
            font-size: 20px !important;
        }

        .text {
            font-size: 16px !important;
        }
    }

    .BackArrow {
        display: flex;
        transform: rotate(0deg);
        transition: transform 0.3s ease;
        justify-content: flex-start;
        align-items: center;
        position: relative;
        top: 4px;
        left: 2px;
    }

    .BackArrow-Down {
        display: flex;
        transform: rotate(90deg);
        transition: transform 0.3s ease;
        justify-content: flex-start;
        align-items: center;
        position: relative;
        top: 4px;
        left: 2px;
    }

    .content {
        display: flex;
        text-align: start;
        font-family: "Montserrat", sans-serif;
        font-size: 1.14583vw;
        font-weight: 500;
        line-height: 26px;
        letter-spacing: 0.21px;
        text-align: left;
        color: #2E3146;
        width: 100%;
        padding-left: 5px;
    }

    .content-dropdown {
        display: flex;
        height: fit-content;
        flex-direction: column;
        padding: 0px 0px 0px 24px;
        border-radius: 15px;
        gap: 6px;
    }
</style>