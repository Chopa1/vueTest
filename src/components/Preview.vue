<script setup>
    import { ref } from 'vue';
    
    const windowWidth = ref(window.innerWidth);
</script>

<template>
    <div class="preview">
        <div class="TextAndPicture">
            <div class="text">
                <h2>Финансовое управление и принципы планирования в здравоохранении</h2>
                <div class="textDescription">
                    <p>
                        На курсе рассматриваются современные представления об экономике здравоохранения и финансовом планировании, 
                        в том числе для ведения междисциплинарных проектов в сфере медицины, экономики и инженерных технологий.
                    </p>
                    <p>
                        На курсе рассматриваются современные представления об экономике здравоохранения и финансовом планировании, 
                        в том числе для ведения междисциплинарных проектов в сфере медицины, экономики и инженерных технологий.
                    </p>
                </div>
            </div>
            <img src="/Rectangle 52.png" v-if = "windowWidth >= 1200">
        </div>

        <div class="teacher">
            <span class="textTeacher">Преподаватели курса:</span>
            <div class="GroupFio">
                <a class="fio" href="#">
                    <img src="/Ellipse 16 (1).png" width="30px">
                    <span class="FioText">А. В. Демакова</span>
                </a>
                <a class="fio" href="#">
                    <img src="/Ellipse 16.png" width="30px">
                    <span class="FioText">А. А. Квасникова</span>
                </a>
                <a class="fio" href="#">
                    <img src="/Ellipse 16 (1).png" width="30px">
                    <span class="FioText">А. А. Красина</span>
                </a>
            </div>

        </div>
    </div>
</template>

<style scoped>

    @import url("https://fonts.googleapis.com/css2?family=Lato:wght@300&display=swap");

    .teacher {
        display: flex;
        justify-content: flex-start;
        border-top: 1px solid rgba(218, 221, 229, 1);
        box-shadow: 0px 0px 30px -10px rgba(70, 73, 94, 0.15);
        padding: 25px 40px 25px 40px;
        gap: 10px;
    }

    .GroupFio {
        display: flex;
        flex-direction: row;
        gap: 22px;
        align-items: center;
        position: relative;
        left: 2px;
        flex-wrap: wrap;
        justify-content: center;
    }

    @media (max-width: 1200px) {
        .GroupFio {
            flex-direction: column;
            align-items: flex-start;
        }

        .teacher {
            flex-direction: column;
            justify-content: start;
        }

        p {
            font-size: 12px !important;
        }

        .text {
            width: 100% !important; 
        }

        h2 {
            font-size: 24px !important;
        }

        .textTeacher {
            font-size: 14px !important;
        }

        .FioText {
            font-size: 14px !important;
        }
    }

    .photo {
        display: flex;
        align-items: center;
    }

    .textDescription {
        display: flex;
        flex-direction: column;
        gap: 22px;
    }

    .FioText {
        font-family: "Montserrat", sans-serif;
        color: rgba(113, 128, 155, 1);
        font-size: 0.83vw;
        font-weight: 500;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
        padding-top: 4px;
        padding-left: 2px;

    }

    .fio {
        display: flex;
        flex-direction: row;
        text-decoration: none;
        gap: 5px;
    }
    .textTeacher {
        display: flex;
        font-family: "Montserrat", sans-serif;
        font-size: 0.8385416vw;
        font-weight: 500;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(46, 49, 70, 1);
        text-align: center;
        white-space: nowrap;
        align-items: center;
    }
    .preview {
        background: rgba(255, 255, 255, 1);
        box-shadow: 0px 0px 30px -10px rgba(70, 73, 94, 0.15);
        border-radius: 10px;
        width: 100%;
        height: fit-content;
        margin: 0px;
        display: flex;
        flex-direction: column;
    }

    .text {
        display: flex;
        flex-direction: column;
        gap: 30px;
        width: 75%;
    }

    .TextAndPicture {
        display: flex;
        flex-direction: row;
        padding: 36px 40px 36px 40px;
        gap: 40px;
    }

    .TextAndPicture img {
        position: absolute;
        right: 41px;
        width: 210px; 
        height: 200px;
    }

    @media (max-width: 1500px) {
        .TextAndPicture img {
        width: 160px; 
        height: 150px;
    }
    }

    h2 {
        font-family: "Montserrat", sans-serif;
        font-size: 1.44247083vw;
        font-weight: 600;
        line-height: 34px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(46, 49, 70, 1);
        margin: 0;
    }

    p {
        font-family: "Montserrat", sans-serif;
        font-size: 0.72916vw;
        font-weight: 400;
        line-height: 20px;
        letter-spacing: 0em;
        text-align: left;
        margin: 0;
    }

    
</style>