<script setup>

import TheButton from '@/UI/TheButton.vue'

</script>

<template>

  <div class="wrap-calculator">

    <div class="calculator-titleBlock">

      <div class="calculator-titleBlock__left">
        <div class="calculator-titleBlock__left-title">
          Рассчитайте стоимость<br>
          лечения зубов
        </div>
        <div class="calculator-titleBlock__left-subTitle">
          Ответьте на 5 вопросов и получите:
        </div>
        <ul class="calculator-titleBlock__left-list">
          <li class="calculator-titleBlock__left-list--item">
            <img src="../../assets/images/СheckIcon.svg" alt="Icon">
            <span>Бесплатную консультацию от <u>стоматолога-кандидата наук</u></span>
          </li>
          <li class="calculator-titleBlock__left-list--item">
            <img src="../../assets/images/СheckIcon.svg" alt="Icon">3 варианта
            стоимости
          </li>
          <li class="calculator-titleBlock__left-list--item">
            <img src="../../assets/images/СheckIcon.svg" alt="Icon">Сюрприз от
            стоматологии
          </li>
        </ul>
      </div>

      <div class="calculator-titleBlock__right">
        <div class="calculator-titleBlock__right-photo-block">
          <img src="../../assets/images/Mg.png" alt="Margarita photo">
          <div>
            <div class="calculator-titleBlock__right-photo-block-name">Маргарита</div>
            <div class="calculator-titleBlock__right-photo-block-proff">Куратор лечения</div>
          </div>
        </div>
        <div class="calculator-titleBlock__right-description">
          После прохождения сориентирует
          по стоимости и ответит на все вопросы.
        </div>
      </div>
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
            <TheButton :isManagementBtn="true">Назад</TheButton>
            <TheButton :isManagementBtn="true" @click="moveLeft">Далее</TheButton>
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

  @include _660 {
    display: flex;
    flex-direction: column;
  }

  margin-bottom: 72px;
}

.calculator-titleBlock {

  display: flex;
  column-gap: 35px;
  justify-content: space-between;

  background-image: linear-gradient(75deg, #DEEFFF, #F9FAFB);
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;

  padding: 40px 24px;



  &__left-title {
    font-weight: 500;
    font-size: 32px;
    line-height: 120%;
    margin-bottom: 24px;
    color: $black-color;
  }

  &__left-subTitle {
    font-weight: 400;
    font-size: 17px;
    line-height: 150%;
    margin-bottom: 32px;
    color: $black-color;
  }

  &__left-list {

    max-width: 296px;

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

  &__right {
    max-width: 40%;

    &-photo-block {

      display: flex;
      column-gap: 14px;
      align-items: center;

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
    }

  }


}

.calculator {

  padding: 40px;

  &-title {
    font-size: 17px;
    line-height: 1.2;
    font-weight: 500;
    color: #111827;
    margin-bottom: 32px;
  }

  &-body {

    display: grid;

    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 12px 8px;

    width: 100%;
    margin-bottom: 32px;

    &-item {
      font-size: 17px;
      line-height: 1.5;
      border-radius: 10px;

      &.one {
        grid-column: 1 / 2;
        grid-row: 1 / 2;
      }

      &.two {
        grid-column: 2 / 3;
        grid-row: 1 / 2;
      }

      &.three {
        grid-column: 1 / 2;
        grid-row: 2 / 3;
      }

      &.four {
        grid-column: 2 / 3;
        grid-row: 2 / 3;
      }

      &.five {
        grid-column: 1 / 3;
        grid-row: 3 / 4;
      }
    }
  }

  &-management {
    display: flex;
    justify-content: space-between;


    &__left {

      padding-bottom: 6px;

      &-title {
        font-size: 14px;
        line-height: 1.2;
        color: #6B7280;
        margin-bottom: 16px;
      }

      &-line {
        width: 230px;
        height: 4px;
        background-color: $primary-color;
      }
    }

    &__right {
      display: flex;
      gap: 8px;
      padding-right: 42px;
    }
  }

}

</style>