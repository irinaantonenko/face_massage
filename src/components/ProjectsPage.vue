<template>
    <div class="projects-page"> 
        <h2 class="projects-page__title">Технології масажу, які я використовую</h2>
        <div class="projects-page__content">
            <projects-page-item
                v-for="project in projects"
                :key="project.id"
                :project="project"
            />
        </div>               
    </div>
</template>

<script>   
    import ProjectsPageItem from "./ProjectsPageItem.vue";
    export default {
        name: 'ProjectsPage',
        data: () => {
            return { 
                projects: [
                {   title: 'Міофасціальний масаж обличчя',
                    text: 'Міофасціальний масаж обличчя – це техніка масажу, яка спрямована на роботу з міофасцією, тобто тканиною, що оточує м`язи та органи. Під час масажу використовуються спеціальні рухи для розслаблення та розтягування цих тканин. Ця техніка може допомогти поліпшити гнучкість м`язів обличчя, зменшити напругу та покращити кровообіг, що сприяє здоров`ю шкіри та загальному вигляду обличчя.',
                    image: 'face7.jpg',
                    id: 1
                },
                {
                    title: 'Спліт-масаж',
                    text: 'Спліт-масаж – це методика мануальної роботи з обличчям. Виконується на «суху», без застосування олії чи крему. Мета Спліт-масажу обличчя усунення тканинних порушень, які виникають на всіх рівнях тканин обличчя та старять обличчя. У Спліт-масажі обличчя використовуються масажні, остеопатичні, фізіотерапевтичні та інші прийоми.',
                    image: 'face8.jpg',
                    id: 2
                },
                {
                    title: 'Апаратний масаж обличчя',
                    text: 'Апаратний масаж обличчя допомагає покращити тонус шкіри, зменшити набряки, стимулювати колагеновий синтез та загалом покращити зовнішній вигляд обличчя. Мікротокова терапія: Використовує слабкі електричні струми для стимуляції м`язів та покращення тонусу шкіри. RF lifting (радіочастотний ліфтинг) обличчя- це неінвазивний косметичний процедурний метод, який використовує радіочастотні хвилі для підтягування та стимуляції колагенових волокон у шкірі обличчя. Основна мета - покращити тонус і еластичність шкіри, зменшити зморшки та підтягнути контури обличчя. Процедура полягає у впливі радіочастотних хвиль на шари шкіри, що призводить до нагрівання тканин. Це сприяє стимуляції вироблення нового колагену та зменшенню втрати еластичності шкіри.',
                    image: 'face10.jpg',
                    id: 3
                },
                {
                    title: 'Лімфодренажний масаж обличчя',
                    text: 'Лімфодренажний масаж обличчя - це техніка масажу, спрямована на стимуляцію лімфатичних вузлів і виведення надлишків рідини з обличчя та шиї. Основна мета - поліпшити лімфатичний потік, зменшити набряки, покращити тонус шкіри та здоров`я обличчя. Процедура використовує легкі рухи, які сприяють дренажу лімфи та сприяють виведенню токсинів. Для лімфодренажу обличчя застосовуються спеціальні техніки, що включають легкі тискання, рухи колом та роботу вздовж ліній лімфатичних судин. Переваги лімфодренажного масажу обличчя включають зменшення набряків, покращення колірної гами шкіри, стимуляцію кровообігу та підтримку загального здоров`я шкіри.',
                    image: 'face5.webp',
                    id: 4
                },
                {
                    title: 'Скульптурний масаж обличчя',
                    text: 'Скульптурний масаж обличчя - це техніка масажу, спрямована на підтягування та формування контурів обличчя, зменшення напруги м`язів і зміцнення тканин. Цей вид масажу часто використовується для покращення форми обличчя і стимуляції колагену. Техніки скульптурного масажу включають в себе легкі згладжуючі рухи, вплив на більші групи м`язів та активізацію лімфатичного дренажу. Зусилля спрямовані на окремі зони обличчя, створюючи відчуття підтягнутості та витонченості. Переваги скульптурного масажу обличчя включають покращення контурів обличчя, зменшення видимості зморшок, підтягнення шкіри та загальне відчуття розслаблення.',
                    image: 'face11.jpg',
                    id: 5
                },
            ]
            }
        },
        components: {
            ProjectsPageItem
        }
    }
</script>

<style lang="scss">
        .projects-page {
            display: flex;
            flex-direction: column;      
            background-color: #ffffff;
            padding-bottom: 50px;
            gap: 50px;       
            border-bottom: 1px solid #ddd;     
            @media (max-width: 425px) {            
                background-color: #fff;
                gap: 20px;  
            }
            &__title {
                font-family: 'Poppins', sans-serif;
                font-size: 36px;                
                padding-top: 50px;
                text-transform: uppercase;
                margin: 0 auto;
                text-align: center;
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
            &__subtitle {
                font-size: 18px;
                margin: 0 auto;
                text-align: center;                 
                padding: 0 10px;            
                @media (max-width: 425px) {
                    font-size: 16px;
                }
            }
            &__content {
                max-width: 100%;
                display: flex;
                align-items: center;
                justify-content: space-around;
                gap: 50px;
                flex-wrap: wrap; 
            }
        }
</style>
