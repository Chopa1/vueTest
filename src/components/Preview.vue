<template>
    <div class="preview">
        <div class="TextAndPicture">
            <div class="text">
                <h2>Финансовое управление и принципы планирования в здравоохранении</h2>
                <p>
                    На курсе рассматриваются современные представления об экономике здравоохранения и финансовом планировании, 
                    в том числе для ведения междисциплинарных проектов в сфере медицины, экономики и инженерных технологий.
                </p>

                <p>
                    На курсе рассматриваются современные представления об экономике здравоохранения и финансовом планировании, 
                    в том числе для ведения междисциплинарных проектов в сфере медицины, экономики и инженерных технологий.
                </p>
            </div>

            <div class="picture">
                <img src="/Rectangle 52.png" width="165px" height="158px">
            </div>
        </div>

        <div class="teacher">
            <span class="textTeacher">Преподаватели курса:</span>
            <div class="GroupFio">
                <a class="fio" href="#">
                    <div class="photo">
                        <img src="/Ellipse 16 (1).png" width="24px">
                    </div>
                    <span class="FioText">А. В. Демакова</span>
                </a>
                <a class="fio" href="#">
                    <div class="photo">
                        <img src="/Ellipse 16.png" width="24px">
                    </div>
                    <span class="FioText">А. А. Квасникова</span>
                </a>
                <a class="fio" href="#">
                    <div class="photo">
                        <img src="/Ellipse 16 (1).png" width="24px">
                    </div>
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
        widows: 100%;
        justify-content: flex-start;
        border-top: 1px solid rgba(218, 221, 229, 1);
        box-shadow: 0px 0px 30px -10px rgba(70, 73, 94, 0.15);
        margin-top: 17px;
        padding: 20px 31px 20px 32px;
        gap: 10px;
    }

    .GroupFio {
        display: flex;
        flex-direction: row;
        gap: 16px;
        align-items: center;
    }

    .photo {
        display: flex;
        align-items: center;
    }

    .FioText {
        font-family: "Montserrat", sans-serif;
        color: rgba(113, 128, 155, 1);
        font-size: 13px;
        font-weight: 500;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;
        padding-left: 3px;
    }

    .fio {
        display: flex;
        flex-direction: row;
        text-decoration: none;
    }
    .textTeacher {
        font-family: "Montserrat", sans-serif;
        font-size: 12.9px;
        font-weight: 500;
        line-height: 22px;
        letter-spacing: 0em;
        text-align: left;

    }
    .preview {
        background: rgba(255, 255, 255, 1);
        box-shadow: 0px 0px 30px -10px rgba(70, 73, 94, 0.15);
        border-radius: 9px;
        width: 100%;
        height: 310px;
        margin: 0px;
        display: flex;
        flex-direction: column;
    }

    .text {
        display: flex;
        flex-direction: column;
        width: 600px;
    }

    .picture {
        padding-left: 41px;
        padding-top: 18px;
    }

    .TextAndPicture {
        display: flex;
        flex-direction: row;
        padding: 12px 32px 0px 33px;
    }

    h2 {
        font-family: "Montserrat", sans-serif;
        font-size: 21.9px;
        font-weight: 600;
        line-height: 27px;
        letter-spacing: 0em;
        text-align: left;
        color: rgba(46, 49, 70, 1);
    }

    p {
        font-family: "Montserrat", sans-serif;
        font-size: 11.06px;
        font-weight: 400;
        line-height: 16px;
        letter-spacing: 0em;
        text-align: left;
        margin-top: 5px;
    }
</style>