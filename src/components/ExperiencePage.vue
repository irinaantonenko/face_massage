<template>
    <div class="experience-page">         
        <div class="experience-page__content">
            <h2 class="experience-page__subtitle">Моя спеціалізація</h2>
            <ul class="experience-page__list" type="disc">
                <li class="experience-page__text">Спліт-масаж, скульптурний масаж, міофасціальний масаж, лімфодренажний масаж, методи для зменшення набряків та тонізації шкіри. Мій підхід базується на індивідуальних потребах кожного клієнта. </li>
                <li class="experience-page__text">Для мене важливо створювати відкриту та довірчу атмосферу, слухаючи ваші потреби та враховати ваші індивідуальні особливості. Ми з вами працюємо на результат!</li>
                <li class="experience-page__text">Я глибоко вірю у потужність масажу обличчя як інструменту для досягнення не лише фізичного благополуччя, але й гармонії всередині. Запрошую вас для покращення вашого зовнішнього вигляду та самопочуття.</li>
            </ul>
        </div>
        <div class="experience-page__image-wrap">
            <img class="experience-page__image" src="../assets/images/face.jpg" alt="about-photo">
        </div> 
    </div>
</template>

<script> 
    export default {
        name: 'AboutMePage'
    }
</script>

<style lang="scss">
        .experience-page {
            display: flex;
            justify-content: space-around; 
            flex-direction: row-reverse;
            min-height: 50vh;
            border-bottom: 1px solid #ddd;
            @media (max-width: 1024px) {
                position: relative;
            }
            @media (max-width: 425px) {
                flex-direction: column;
                padding: 20px 0;
                background-color: #F6F6F6;
            }
            &__content {
                width: 50%;
                display: flex;
                flex-direction: column;
                align-items: flex-start; 
                gap: 20px;
                //@media (max-width: 1024px) {
                 //   width: 30%;
                //}
                //@media (max-width: 600px) {
                //    width: 45%;
                //}
                @media (max-width: 425px) {
                    width: 100%;
                    align-items: center;
                    padding: 0 30px;
                }
            }
            &__subtitle {
                font-family: 'Poppins', sans-serif;
                font-size: 36px;
                padding: 50px 0 20px;
                text-transform: uppercase;
                text-align: center;
                @media (max-width: 1440px) {
                    font-size: 26px;
                }
                @media (max-width: 768px) {
                    font-size: 20px;
                }
                @media (max-width: 425px) {
                    padding-top: 0;
                }
            }
            &__list {
                padding-bottom: 20px;
                list-style: none;
            }
            &__text {
                font-size: 22px;
                padding-bottom: 20px;
                display: flex;
                gap: 10px;
                @media (max-width: 1960px) {
                    padding-bottom: 10px;
                }
                @media (max-width: 1440px) {
                    font-size: 18px;
                }
                @media (max-width: 768px) {
                    padding-bottom: 5px;
                }
                @media (max-width: 500px) {
                    font-size: 14px;
                }
            }
            &__image-wrap {
                position: relative;
                width: 30%;
                min-width: 200px;
                max-height: 800px;
                overflow: hidden;
                padding: 50px 0;
                @media (max-width: 425px) {
                    margin: 0 auto;
                }
            }
            &__image {
                width: 100%;
                height: 100%;
                object-fit: contain;
                object-position: center left;
                
            }
        }
</style>
