<template>
    <div class="theme">
        <div class="name" @click="toggleDropdown">
            <div :class="{'BackArrow': !showContent, 'BackArrow-Down': showContent}">
                <IconArrowTheme />
            </div>
            <span class="content">{{ themeName }}</span>
            <div v-if="all" class="all">
                <span class="allTheme">Свернуть всё</span>
            </div>
        </div>
        <div v-if="showContent" class="content-dropdown">
            <div class="title">
                <p class="text">Материалы для изучения</p>
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
        width: 100%;
        border-radius: 9px;
        padding: 24px 0px 17px 0px;
        flex-direction: column;
    }

    .all {
        display: flex;
        z-index: 1;
        padding-right: 66px;
    }

    .allTheme {
        display: flex;
        white-space: nowrap;
        font-family: "Montserrat", sans-serif;
        font-size: 12.6px;
        font-weight: 400;
        line-height: 16px;
        letter-spacing: 0em;
        text-align: right;
        color: rgba(39, 55, 102, 1);
    }

    .title {
        display: flex;
        padding: 29px 20px 10.5px 16px;
        color: rgba(46, 49, 70, 1);
    }

    .text {
        display: flex;
        font-family: "Montserrat", sans-serif;
        font-size: 12.7px;
        font-weight: 400;
        line-height: 24px;
        letter-spacing: 0em;
        text-align: left;
        margin: 0;
        color: rgba(46, 49, 70, 1);
    }

    .name {
        display: flex;
        gap: 11px;
        cursor: pointer;
        align-items: center;
        align-items: flex-start;
        width: 100%;
        padding: 0px 40px 0px 26.6px;
    }

    .BackArrow {
        display: flex;
        transform: rotate(0deg);
        transition: transform 0.3s ease;
        justify-content: flex-start;
    }

    .BackArrow-Down {
        display: flex;
        transform: rotate(90deg);
        transition: transform 0.3s ease;
        justify-content: flex-start;
    }

    .content {
      display: flex;
      text-align: start;
      font-family: "Montserrat", sans-serif;
      font-size: 17.7px;
      font-weight: 500;
      line-height: 20.7px;
      letter-spacing: 0em;
      color: #2E3146;
      padding-bottom: 2px;
      width: 88%;
    }

    .content-dropdown {
        display: flex;
        padding-left: 43px;
        flex-direction: column;
    }


</style>