<script setup>

import TheButton from '../UI/TheButton.vue'
</script>

<template>
  <div class="careSliderTitle">
    Вы окутаны заботой
  </div>
  <div class="careSliderSubTitle">
    Куратор лечения - это специалист, который будет сопровождать вас на протяжении всего лечения, оказывая поддержку и
    руководство.
  </div>
  <div class="careSlider">
    <div class="careSlider__card">
      <div class="careSlider__card-left">
        <div class="careSlider__card-left_title">
          Седовласова Юлия
        </div>
        <div class="careSlider__card-left_experience">
          Стаж: <span>6 лет</span>
        </div>
        <ul class="careSlider__card-left_list">
          <li>По-человечески поддержит вас</li>
          <li>Объяснит то, что не понятно после приема — переведет с медицинского языка на человеческий.</li>
          <li>Поможет разобраться с планом лечения</li>
          <li>Подберет все возможные и невозможные способы оплат</li>
          <li>Постоянно на связи</li>
        </ul>
        <TheButton :isBluBtn="true">Записаться на приём</TheButton>
      </div>
      <div class="careSlider__card-right">
        <img src="../assets/images/careSlider/cart1.png" alt="cart1">
      </div>
    </div>
    <div class="careSlider__menage">
      <TheButton :isCareSlider="true">Назад</TheButton>
      <TheButton :isCareSlider="true">Далее</TheButton>
    </div>
  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";


.careSliderTitle {
  color: $primary-color;
  font-size: 53px;
  font-weight: 700;
  text-align: center;
  line-height: 93%;
  margin-bottom: 16px;
}

.careSliderSubTitle {
  color: $black-color;
  font-size: 17px;
  line-height: 150%;
  max-width: 50%;
  margin: 0 auto 40px;
}

.careSlider {

  margin-bottom: 96px;

  &__menage {
    display: flex;
    justify-content: center;
    column-gap: 12px;
    padding: 12px 0 16px;
  }

  &__card {

    display: flex;
    column-gap: 8px;
    max-height: 463px;

    &-left {

      background: linear-gradient(to bottom, rgba(232, 244, 252, 0.35) 0%, rgba(236, 245, 254, 0.91) 4%, rgba(236, 245, 254, 1) 5%, rgba(237, 246, 254, 0.99) 100%);
      border-radius: 16px;
      padding: 56px;

      &_title {
        font-size: 28px;
        font-weight: 500;
        line-height: 120%;
        letter-spacing: 0.3px;
        margin-bottom: 24px;
      }

      &_experience {
        color: #4D5561;
        margin-bottom: 24px;

        span {
          color: #111C27;
          font-weight: 700;
        }
      }

      &_list {

        margin-bottom: 26px;

        li {
          position: relative;
          margin-bottom: 16px;
          margin-left: 15px;
        }

        li::before {
          content: "";
          width: 4px;
          height: 4px;
          border-radius: 50%;
          background-color: #30B5DF;
          position: absolute;
          left: -15px;
          top: 7px;
        }
      }
    }

    &-right {
      img {
        display: block;
        max-width: 401px;
      }
    }

  }

}


</style>