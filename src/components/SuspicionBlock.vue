<script setup>

import TheButton from '../UI/TheButton.vue'
</script>

<template>
  <div class="suspicionBlock">
    <div class="suspicionBlock__title">
      С чего начать, если <span>есть сомнения?</span>
    </div>
    <div class="suspicionBlock__card">
      <div class="suspicionBlock__card--item">
        <div class="suspicionBlock__card--item_title">
          Обсудить вашу ситуацию
        </div>
        <div class="suspicionBlock__card--item_descr">
          Ответим на все вопросы, предложим
          варианты лечения, сориентируем
          по стоимости.
        </div>
        <TheButton :isSuspicionBtb="true">Получить консультацию</TheButton>
        <img src="../assets/images/iPhone.png" alt="iPhone">
      </div>
      <div class="suspicionBlock__card--item">
        <div class="suspicionBlock__card--item_title">
          Ознакомится с презентацией
        </div>
        <div class="suspicionBlock__card--item_descr">
          Описание всех услуг и цен, чтобы после разговора ознакомится
          со всем лично.
        </div>
        <TheButton :isSuspicionBtb="true">Получить презентацию</TheButton>
        <img src="../assets/images/Macbook.png" alt="MacBook">
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">

.suspicionBlock {

  margin-bottom: 174px;

  &__title {
    font-size: 48px;
    line-height: 1;
    font-weight: 700;
    margin-bottom: 40px;

    span {
      color: #30B5DF;
    }
  }

  &__card {
    display: flex;
    justify-content: space-between;
    column-gap: 32px;

    &--item {

      border-radius: 16px;
      width: 100%;
      background: linear-gradient(to bottom, rgba(232, 244, 252, 0.35) 0%, rgba(236, 245, 254, 0.91) 4%, rgba(236, 245, 254, 1) 5%, rgba(237, 246, 254, 0.99) 100%);

      //background-color: goldenrod;
      padding: 32px 0 104px 32px;

      position: relative;


      &_title {
        font-size: 22px;
        line-height: 32.64px;
        font-weight: 700;
        color: #001837;
        margin-bottom: 12px;
      }

      &_descr {
        font-size: 15px;
        line-height: 1.5;
        color: #001E45;
        margin-bottom: 24px;
        max-width: 280px;
      }

      &:first-child {
        img {
          display: block;
          max-width: 161px;
          position: absolute;
          bottom: 0;
          right: 32px;
        }
      }

      &:last-child {
        img {
          display: block;
          max-width: 253px;
          position: absolute;
          bottom: 10px;
          right: 0;
        }
      }
    }
  }
}

</style>