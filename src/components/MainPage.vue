<template>
    <div class="main-page">  
        <div class="main-page__content">
            <h1 class="main-page__title">Наталя Гайдаш</h1>            
            <h2 class="main-page__subtitle">Фахівець з масажу обличчя</h2>
            <p class="main-page__text">Вітаю! Я - Наталя Гайдаш, і я є сертифікованим фахівцем з масажу обличчя з медичною освітою, спеціалізуюсь на створенні унікальних та дієвих масажних сесій.
                Маю великий практичний досвід у сфері масажу обличчя, працюючи з різними клієнтами та враховуючи їхні індивідуальні потреби та побажання. Міксую та ефективно використовую різноманітні техніки для досягнення бажаних результатів.
            </p>
        </div>
        <div class="main-page__image-wrap">
            <img src="../assets/images/salon.webp" alt="main" class="main-page__image">
        </div>
    </div>
</template>

<script>  
    export default {
        name: 'MainPage',
    }
</script>

<style lang="scss">
    .main-page {
        display: flex;
        align-items: center;
        justify-content: space-between; 
        flex-direction: reverse;      
        background-color: #Fffff5;
        min-height: 80vh;
        @media (max-width: 935px) {
            flex-direction: column;
        }
        &__content {
            width: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 50px;
            min-height: 600px;
            position: absolute;
            z-index: 55;
            @media (max-width: 935px) {
                width: 100%;
                min-height: 100vh;
                gap: 20px;
            }
            @media (max-width: 768px) {
                gap: 30px;
            }
        }
        &__subtitle {
            font-size: 22px;
            text-transform: uppercase;
            @media (max-width: 425px) {
                font-size: 14px;
            }
        }
        &__title {
            font-family: 'Poppins', sans-serif;
            font-size: 60px;
            text-align: center;
            @media (max-width: 500px) {
                font-size: 40px;
            }
            @media (max-width: 935px) {
                font-size: 50px;
            }
            @media (max-width: 425px) {
                font-size: 40px;
                margin-bottom: 0;
            }
        }
        &__text {
            width: 400px;
            font-size: 22px;
            @media (max-width: 1440px) {
                font-size: 20px;
            }
            @media (max-width: 935px) {
                width: 500px;
                font-size: 18px;
            } 
            @media (max-width: 590px) {
                width: 80%;
            }
            @media (max-width: 500px) {
                font-size: 14px;
            }
        }
        &__mail {
            text-transform: uppercase;
            text-decoration: none;
            padding-bottom: 10px;
            border-bottom: 1px solid #000;
            color: #000;
            &:hover {
                color: red;
                border-bottom: 1px solid red;
            }
        }
        &__image-wrap {
            position: relative;
            width: 100%;
            min-height: 100vh;
            overflow: hidden;
        }
        &__image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position:center;
            position: absolute;
        }
    }
</style>
