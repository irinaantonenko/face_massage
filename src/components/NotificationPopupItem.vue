<template>
    <div class="popup__wrapper" ref="popup_wrapper">
        <div class="popup" id="myModal">            
            <div class="popup__header">
              <h3 class="popup__title">{{ project.title }}</h3>
              <img class="popup__image" :src="require('../assets/images/' + project.image)" alt="">
              
              <span class="icon-cross popup__icon" @click="closePopup"></span>
            </div>
            <div class="popup__content">
              <p class="popup__text">{{ project.text }}</p>
              <!-- <button class="popup__btn btn" @click="closePopup">Оk</button> -->
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'NotificationPopupItem',
  props: {
    project: {
      type: Object,
      default() {
          return {}
      }
    }
  },
  methods: {
    closePopup() {
      this.$emit('closePopup');
    },
  },
  mounted() {
    let vm = this;
    document.addEventListener('click', function (event) {
      if (event.target === vm.$refs['popup_wrapper']) {
        vm.closePopup();
      }
    });
  },
};
</script>

<style lang="scss">
   .popup {
      padding: 60px 30px 30px;
      position: fixed;
      width: 800px;
      box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.8);
      z-index: 1000;
      border-radius: 10px;
      background-color: rgb(196, 220, 168);
      @media (max-width: 900px) {
        width: 90%;
      }
      &__wrapper {
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: rgba(0, 0, 0, 0.6);
        position: fixed;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        z-index: 1433;
        height: 100%;
        width: 100%;
        overflow-x: hidden;
        overflow-y: auto;
        transition: opacity .15s linear;
      }
      &__header {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
      }
      &__image {
        width: 150px;
        height: 220px;
        border-radius: 50%;
        @media (max-width: 900px) {
          width: 50px;
          height: 80px;
        }
      }
      &__title {
        color: #fff;
        text-align: center;
        padding-bottom: 25px;
        font-size: 22px;
      }
      &__content {
          display: flex;
          justify-content: center;
          align-items: center;
          flex-direction: column;
          & .login-form__input {
              width: 440px;
              @media (max-width: 700px) {
                  width: 100%;
              }
          }
      }
      &__text {
        background-color: #fff;
        border-radius: 10px;
        margin-top: 20px;
        padding: 20px;
        font-size: 18px;
        @media (max-width: 900px) {
          font-size: 14px;
        }
      }
      &__icon {
          color: #fff;
          cursor: pointer;
          position: absolute;
          z-index: 1111;
          font-size: 17px;
          top: 15px;
          right: 15px;
          &:hover {
              opacity: 0.8;
          }
      }
      &__btn.btn {
      }
    }
    .modal-open {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow-y: hidden;
    }   
</style>