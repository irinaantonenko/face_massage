<template>
    <div class="plus-page">         
        <div class="plus-page__content">
            <h2 class="plus-page__subtitle">Масаж обличчя має численні переваги для здоров'я та зовнішнього вигляду. Деякі з цих переваг включають:</h2>
            <ul class="plus-page__list" type="disc">
                <li class="plus-page__text"><b>1. Розслаблення м'язів:</b> Масаж допомагає розслабити напружені м'язи обличчя, зменшуючи відчуття напруги та стресу.</li>
                <li class="plus-page__text"><b>2. Покращення кровообігу:</b> Масаж сприяє поліпшенню кровообігу, що призводить до кращого здоров'я шкіри та подавання кисню та поживних речовин клітинам.</li>
                <li class="plus-page__text"><b>3. Зменшення набряків:</b> Легкі масажні рухи допомагають виводити зайву рідину, зменшуючи набряки та пухкість обличчя.</li>
                <li class="plus-page__text"><b>4. Стимуляція колагену:</b> Масаж може сприяє виробленню колагену, що важливо для збереження тонусу та еластичності шкіри.</li>
                <li class="plus-page__text"><b>5. Зняття стресу:</b> Регулярний масаж обличчя сприяє зняттю стресу та розслабленню, поліпшуючи загальний настрій.</li>
                <li class="plus-page__text"><b>6. Підтримка здоров'я шкіри:</b> Масаж сприяє видаленню відмерлих клітин шкіри, покращенню текстури та вигляду обличчя.</li>
                <li class="plus-page__text"><b>7. Підвищення тонусу м'язів обличчя:</b> Регулярні масажні процедури сприяють підтримці тонусу м'язів, що допомагає у попередженні опущення шкіри.</li>
            </ul>
            <p class="plus-page__text">Важливо враховувати, що ефективність масажу обличчя може варіювати в залежності від індивідуальних особливостей та методів, що використовуються.</p>
        </div>
        <div class="plus-page__image-wrap">
            <img class="plus-page__image" src="../assets/images/facemassage.jpg" alt="about-photo">
        </div> 
    </div>
</template>

<script> 
    export default {
        name: 'PlusPage'
    }
</script>

<style lang="scss">
        .plus-page {
            display: flex;
            justify-content: space-around; 
            min-height: 50vh;
            border-bottom: 1px solid #ddd;
            padding-bottom: 50px;
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
               //     width: 30%;
                //}
                //@media (max-width: 600px) {
                 //   width: 45%;
                //}
                @media (max-width: 1200px) {
                    width: 100%;
                    padding: 0 50px;
                }
                @media (max-width: 425px) {
                    width: 100%;
                    align-items: center;
                    padding: 0 30px;
                }
            }
            &__subtitle {
                //font-family: 'Libre Baskerville';
                font-family: 'Poppins', sans-serif;
                font-size: 22px;
                padding: 50px 0 20px;
                text-transform: uppercase;
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
                @media (max-width: 1200px) {
                    display: none;
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
