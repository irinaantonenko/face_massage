<template>
    <div class="contact-page"> 
        <div class="contact-page__image-wrap">
            <img src="../assets/images/fm.jpg" alt="contact" class="contact-page__image">
        </div>
        <div class="contact-page__content">
            <h2 class="contact-page__title">Зв'яжись зі мною</h2>
            <div class="contact-page__btns">
                <a href="https://t.me/face_massage_ua" target="_blank" class="contact-page__link">
                    <span class="icon-telegram"></span>
                    <p class="contact-page__text">Telegram</p>  
                </a>
                <a href="https://msng.link/o/?380958879988=vi" target="_blank" class="contact-page__link">
                    <span class="icon-viber"></span>
                    <p class="contact-page__text">Viber</p>  
                </a>
                <a href="https://www.instagram.com/face.massage.ua?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==" target="_blank" class="contact-page__link">
                    <span class="icon-instagram"></span>
                    <p class="contact-page__text">Instagram</p>  
                </a>
            </div>
        </div>
    </div>
</template>

<script>    
    export default {
        name: 'ContactPage'
    }
</script>
<style lang="scss">
    .contact-page {
        display: flex;
        align-items: center;
        justify-content: space-around;
        min-height: 50vh;
        padding-bottom: 50px;
        @media (max-width: 1440px) {
            padding-bottom: 0;
        }
        @media (max-width: 500px) {
            flex-direction: column-reverse;
        }
        &__image-wrap {
            position: relative;
            width: 30%;
            min-width: 200px;
            max-height: 800px;
            overflow: hidden;
            padding: 50px 0;
        }
        &__image {
            width: 100%;
            height: 100%;
            object-fit: contain;
            object-position: center left;
        }
        &__content {
            width: 50%;
            display: flex;
            align-items: center;
            flex-direction: column;
            gap: 50px;
            padding: 50px 0 20px;
            @media (max-width: 935px) {
                gap: 20px;
            }
            @media (max-width: 425px) {
                padding-top: 20px;
                width: 100%;
            }
        }
        &__title {
            font-family: 'Poppins', sans-serif;
            font-size: 36px;  
            text-transform: uppercase;
            margin: 0 auto;
            @media (max-width: 1440px) {
                font-size: 26px;
            }
            @media (max-width: 768px) {
                font-size: 20px;
            }
            @media (max-width: 425px) {
                padding-top: 20px;
            }
        }
        &__btns {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }
        &__link {
            text-decoration: none;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid #ddd;
            box-sizing: border-box;
            border-radius: 5px;
            gap: 10px;
            width: 160px;
            height: 50px;
            color: #000;
            cursor: pointer;
            font-size: 22px;
            &:hover {
                opacity: 0.5;
            }
            @media (max-width: 768px) {
                font-size: 14px;
            }
        }
        &__resume {
            background-color: #d14836;
            color: #fff;
            cursor: pointer;
            font-size: 18px;
            text-decoration: none;
            width: 250px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 5px;
            &:hover {
                opacity: 0.7;
            }
            @media (max-width: 768px) {
                font-size: 14px;
                width: 200px;
            }
        }
    }
</style>