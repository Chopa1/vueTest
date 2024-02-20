<template>
    <div class="theme">
        <div class="name" @click="toggleDropdown">
            <div :class="{'BackArrow': !showContent, 'BackArrow-Down': showContent}">
                <IconArrowTheme />
            </div>
            <span class="content">{{ themeName }}</span>
        </div>
        <div v-if="showContent" class="content-dropdown">
            <div class="title">
                <p class="text">Материалы для изучения</p>
            </div>
            <References />
            <ReferenceFile :themeBool="false"/>

            <div class="full2">
                <ReferenceFile :themeBool="false"/>
                <div class="info2">
                    <IconLock />
                    <div class="fullText2">
                        <span class="text2">Недоступно, пока не выполнено: Элемент курса</span>
                        <span class="text2">Задание должен быть отмечен как выполненный</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import IconArrowTheme from './icons/IconArrowTheme.vue';
    import References from './References.vue';
    import ReferenceFile from './ReferenceFile.vue';
    import IconLock from './icons/IconLock.vue';

    import { defineProps } from 'vue';
    
    const showContent = ref(true);
    
    const toggleDropdown = () => {
        showContent.value = !showContent.value;
    };

    const props = defineProps({
        themeName: String,
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
        padding: 34.5px 0px 34.5px 0px;
        flex-direction: column;
    }

    .title {
        display: flex;
        padding: 28.4px 20px 10px 15px;
        color: rgba(46, 49, 70, 1);
    }

    .info2 {
        display: flex;
        position: relative;
        top: -7px;
        flex-direction: row;
        background: rgba(233, 237, 244, 0.4);
        padding: 9.5px 9.6px 8px 9.6px;
        align-items: center;
        gap: 8.5px;
        border-radius: 5px;
        margin-left: 15px;
        margin-right: 40px;
    }

    .fullText2 {
        display: flex;
        flex-direction: column;
        gap: 3.5px;
    }

    .text2 {
        font-family: "Montserrat", sans-serif;
        font-size: 9.5px;
        font-weight: 500;
        line-height: 11.5px;
        letter-spacing: 0em;
        text-align: left;
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
        padding: 0px 40px 0px 26px;
    }

    .BackArrow {
        display: flex;
        transform: rotate(0deg);
        transition: transform 0.3s ease;
        justify-content: flex-start;
        background: rgba(233, 242, 255, 0.4);
        border-radius: 30px;
    }

    .BackArrow-Down {
        display: flex;
        transform: rotate(90deg);
        transition: transform 0.3s ease;
        justify-content: flex-start;
        background: rgba(233, 242, 255, 0.4);
        border-radius: 30px;
    }

    .content {
      display: flex;
      align-items: center;
      font-family: "Montserrat", sans-serif;
      font-size: 17.7px;
      font-weight: 500;
      line-height: 20.6px;
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