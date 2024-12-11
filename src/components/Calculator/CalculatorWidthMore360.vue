<script setup>

import TheButton from '@/UI/TheButton.vue'

</script>

<template>

  <div class="wrap-calculator">

    <div class="calculator-titleBlock">

      <div class="calculator-titleBlock-title">
        Рассчитайте стоимость<br>
        лечения своих зубов
      </div>

      <div class="calculator-titleBlock-photo-block">
        <img src="../../assets/images/Mg.png" alt="Margarita photo">
        <div>
          <div class="calculator-titleBlock-photo-block-name">Маргарита</div>
          <div class="calculator-titleBlock-photo-block-proff">Куратор лечения</div>
        </div>
      </div>

      <div class="calculator-titleBlock-description">
        После прохождения сориентирует
        по стоимости и ответит на все вопросы.
      </div>

      <div class="calculator-titleBlock-subTitle">
        Ответьте на 5 вопросов и получите:
      </div>

      <ul class="calculator-titleBlock-list">
        <li class="calculator-titleBlock-list--item">
          <img src="../../assets/images/СheckIcon.svg" alt="Icon">
          <span>Бесплатную консультацию от <u>стоматолога-кандидата наук</u></span>
        </li>
        <li class="calculator-titleBlock-list--item">
          <img src="../../assets/images/СheckIcon.svg" alt="Icon">3 варианта
          стоимости
        </li>
        <li class="calculator-titleBlock-list--item">
          <img src="../../assets/images/СheckIcon.svg" alt="Icon">Сюрприз от
          стоматологии
        </li>
      </ul>


    </div>

    <div class="calculator">

      <div class="calculator-slide_1">

        <div class="calculator-title">
          Сколько зубов нуждаются в лечении?
        </div>

        <ul class="calculator-body">
          <li class="calculator-body-item one">
            <TheButton :isCalcBtn="true">1</TheButton>
          </li>
          <li class="calculator-body-item two">
            <TheButton :isCalcBtn="true">2</TheButton>
          </li>
          <li class="calculator-body-item three">
            <TheButton :isCalcBtn="true">3</TheButton>
          </li>
          <li class="calculator-body-item four">
            <TheButton :isCalcBtn="true">4 и более</TheButton>
          </li>
          <li class="calculator-body-item five">
            <TheButton :isCalcBtn="true">Точно не знаю</TheButton>
          </li>
        </ul>


        <div class="calculator-management">
          <div class="calculator-management__left">
            <div class="calculator-management__left-title">3 из 5</div>
            <div class="calculator-management__left-line"></div>
          </div>
          <div class="calculator-management__right">
            <TheButton class="managementBtn" :isManagementBtn="true">Назад</TheButton>
            <TheButton class="managementBtn" :isManagementBtn="true" @click="moveLeft">Далее</TheButton>
          </div>
        </div>


      </div>
    </div>

  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.wrap-calculator {

  border: 1px solid #D1D6DB;
  border-radius: 20px;

  margin-bottom: 60px;

}

.calculator-titleBlock {

  display: flex;
  flex-direction: column;

  background-image: linear-gradient(75deg, #DEEFFF, #F9FAFB);
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;

  padding: 40px 16px;

  &-title {
    font-weight: 500;
    font-size: 30px;
    line-height: 125%;
    margin-bottom: 24px;
    color: $black-color;
  }

  &-photo-block {

    display: flex;
    align-items: center;
    column-gap: 14px;

    margin-bottom: 24px;

    img {
      max-width: 62px;
    }

    &-name {
      font-weight: 700;
      font-size: 17px;
      line-height: 140%;
    }

    &-proff {
      font-size: 15px;
      color: #6B7280;
    }
  }


  &-description {
    font-weight: 400;
    font-size: 17px;
    line-height: 150%;
    margin-bottom: 40px;
  }

  &-subTitle {
    font-weight: 600;
    font-size: 17px;
    line-height: 150%;
    margin-bottom: 10px;
  }

  &-list {

    &--item {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 16px;
    }

    &--item:last-child {
      margin-bottom: 0;
    }
  }
}

.calculator {

  padding: 40px 16px 32px;

  &-title {
    font-size: 17px;
    line-height: 1.2;
    font-weight: 500;
    color: #111827;
    margin-bottom: 32px;
    text-align: center;
  }

  &-body {

    width: 100%;
    margin-bottom: 32px;

    &-item {
      font-size: 17px;
      line-height: 1.5;
      border-radius: 10px;
      margin-bottom: 8px;
    }
  }

  &-management {

    display: flex;
    flex-direction: column;

    &__left {

      padding-bottom: 6px;

      &-title {
        font-size: 14px;
        line-height: 1.2;
        color: #6B7280;
        margin-bottom: 16px;
      }

      &-line {
        width: 100%;
        height: 4px;
        background-color: $primary-color;
        margin-bottom: 32px;
      }
    }

    &__right {
      display: flex;
      justify-content: right;
      column-gap: 8px;

      @media (max-width: 450px) {
        justify-content: center;
      }
    }

  }

  .managementBtn {
    padding: 22px 47px;
  }

}

</style>