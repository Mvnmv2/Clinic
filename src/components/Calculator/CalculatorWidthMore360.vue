<script setup>

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

    <div class="calculator-body">
      123456
    </div>


  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.wrap-calculator {
  border: 1px solid #D1D6DB;
  border-radius: 20px;
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

      &-prof {
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
</style>