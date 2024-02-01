<template>
    <notification-popup-item
        v-if="notificationShow"
        @closePopup="closeNotificationPopup"
        :project="project"
    />
    <a @click="openModal(project)" target="_blank" :href="project.link" class="projects-item">   
        <div class="projects-item__image-wrap">        
            <img class="projects-item__image" :src="require('../assets/images/' + project.image)" alt="projects-photo">
        </div>
        <p class="projects-item__subtitle">{{ project.title }}</p>                
    </a>
</template>

<script>   
    import NotificationPopupItem from './NotificationPopupItem.vue';
    export default {
        name: 'ProjectsPageItem',
        components: {NotificationPopupItem},
        data() {
            return {
                notificationShow: false,
            };
        },
        props: {
            project: {
                type: Object,
                default() {
                    return {}
                }
            }
        },
        methods: {
            openModal() {
                this.notificationShow = true;
                document.body.classList.add('modal-open');
            },
            closeNotificationPopup() {
                this.notificationShow = false;
                document.body.classList.remove('modal-open');
            },
        }
    }
</script>

<style lang="scss">
    .projects-item {
        display: flex;
        flex-direction: column;
        justify-content: stretch;
        flex-basis: 20%;
        box-shadow: 0 0 5px 5px rgb(196 220 168);
        border-radius: 20px;
        overflow: hidden;
        cursor: pointer;
        min-width: 260px;
        position: relative;
        text-decoration: none;
        &:hover {
            box-shadow: 0 0 7px 10px rgb(196 220 168);
        }
        &:hover &__subtitle {
            color: green;
        }
        &__image-wrap {
            position: relative;
            width: 100%;
            padding-top: 60%;
        }
        &__image {
            width: 100%;
            height: 100%;
            opacity: 0.9;
            position: absolute;
            top: 10px;
            padding-bottom: 10px;
            left: 0;
            object-fit: contain;
            object-position: center;
            &:hover {
                opacity: 1;
            }
        }
        &__subtitle {
            padding: 10px;
            font-size: 20px;
            margin: 0 auto;
            color: #000;                            
            min-height: 70px;
            text-align: center;
            @media (max-width: 1440px) {
                font-size: 18px;
            }
            @media (max-width: 425px) {
                font-size: 16px;
            }
        }
    }
</style>