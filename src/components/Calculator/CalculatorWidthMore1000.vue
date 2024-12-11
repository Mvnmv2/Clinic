<script setup>

import TheButton from '@/UI/TheButton.vue'

</script>

<template>

  <h2 class="title-calculator">Рассчитайте стоимость лечения своих зубов</h2>

  <div class="wrap-calculator">

    <div class="info-calculator">
      <div class="info-calculator__block">
        <div class="info-calculator__block-title">
          <div class="info-calculator__block-photo-block">
            <img src="../../assets/images/Mg.png" alt="Margarita photo">
            <div>
              <div class="info-calculator__block-name">Маргарита</div>
              <div class="info-calculator__block-proff">Куратор лечения</div>
            </div>
          </div>

          <div class="info-calculator__block-description">После прохождения сориентирует
            по стоимости и ответит на все вопросы.
          </div>
        </div>
        <div class="info-calculator__block-list-title">
          Ответьте на 5 вопросов и получите:
        </div>
        <ul class="info-calculator__block-list">
          <li class="info-calculator__block-list-item">
            <img src="../../assets/images/СheckIcon.svg" alt="Icon">
            <span>Бесплатную консультацию от <u>стоматолога-кандидата наук</u></span>
          </li>
          <li class="info-calculator__block-list-item"><img src="../../assets/images/СheckIcon.svg" alt="Icon">3 варианта
            стоимости
          </li>
          <li class="info-calculator__block-list-item"><img src="../../assets/images/СheckIcon.svg" alt="Icon">Сюрприз от
            стоматологии
          </li>
        </ul>
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

      </div>

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

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables.scss";

.title-calculator {
  font-size: 32px;
  font-weight: 500;
  line-height: 1.25;
  text-align: center;
  margin-bottom: 40px;
}

.wrap-calculator {
  display: flex;
  column-gap: 8px;
  //height: 470px;
  margin-bottom: 96px;
}

.info-calculator {
  max-width: 407px;

  background-image: linear-gradient(75deg, #DEEFFF, #F9FAFB);
  border: 1px solid #D1D6DB;
  border-radius: 20px;

  padding-top: 48px;
  padding-left: 48px;
  padding-right: 35px;
}

.info-calculator__block {

  &-photo-block {
    display: flex;
    align-items: center;
    column-gap: 14px;
    margin-bottom: 24px;

    img {
      display: block;
      max-width: 62px;
    }
  }

  &-name {
    font-size: 17px;
    line-height: 1.4;
    font-weight: 900;
    color: #111C27;
  }

  &-proff {
    font-size: 15px;
    font-weight: 400;
    line-height: 1.4;
    color: #6B7280;
  }

  &-description {
    font-size: 17px;
    line-height: 1.4;
    margin-bottom: 32px;
    color: #111827;
  }

  &-list-title {
    font-size: 17px;
    line-height: 1.5;
    font-weight: 900;
    color: #111C27;
    margin-bottom: 16px;
  }
}

.info-calculator__block-list {
  &-item {
    display: flex;
    align-items: center;
    column-gap: 12px;
    margin-bottom: 16px;
  }
}

.calculator {
  border: 1px solid #D1D6DB;
  border-radius: 20px;
  width: 100%;

  padding-top: 82px;
  padding-bottom: 90px;

  text-align: center;

  display: grid;
  justify-content: center;

  &-title {
    font-size: 20px;
    line-height: 1.2;
    font-weight: 900;
    color: #111827;
    margin-bottom: 32px;
    margin-left: 75px;
  }

  &-body {

    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 12px 8px;

    width: 511px;
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