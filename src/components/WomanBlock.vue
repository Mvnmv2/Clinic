<script setup>

import TheButton from '../UI/TheButton.vue'
</script>


<template>
  <div class="container-2">
    <div class="womanBlock">

      <img class="womanBlock__img" src="../assets/images/woman.png" alt="woman img">

      <div class="womanBlock__titleBlock">
        <div class="womanBlock__titleBlock-title">
          Новые зубы по цене<br>
          <span>чашки кофе в день</span>
        </div>
        <p>В стоматологии Ami Clinic лечение доступно каждому
          без мнимой экономии!
        </p>
        <p>Следите за здоровьем зубов у ведущих специалистов Москвы на самых гибких условиях.</p>
      </div> <!--womanBlock__titleBlock-->

      <div class="womanBlock__cards">

        <div class="womanBlock__cards-item">
          <div class="womanBlock__cards-item-wrapper">
            <div class="womanBlock__cards-item--title">
              Рассрочка от Ami Clinic
            </div>
            <ul class="womanBlock__cards-list">
              <li>6 месяцев</li>
              <li>От 300 руб. в день</li>
              <li>Оформление на месте</li>
            </ul>
            <TheButton :isBluBtn="true">Узнать подробнее</TheButton>
          </div>
          <img src="../assets/images/Logo1.png" alt="Logo1">
        </div>

        <div class="womanBlock__cards-item">
          <div class="womanBlock__cards-item-wrapper">
            <div class="womanBlock__cards-item--title">
              Рассрочка от 25 банков-партнеров
            </div>
            <ul class="womanBlock__cards-list">
              <li>Одобряемость 90% прямо на консультации</li>
              <li>Без первоночального взноса до 12 мес.</li>
              <li>С первоночальным взносом до 24 мес.</li>
            </ul>
            <TheButton :isBluBtn="true">Узнать подробнее</TheButton>

          </div>
          <img src="../assets/images/Logo2.png" alt="Logo2">

        </div>

      </div> <!--womanBlock__cards-->
    </div> <!--womanBlock-->
  </div> <!--container-2-->

</template>

<style scoped lang="scss">

.container-2 {
  width: 100%;
  max-width: 1440px;

  margin: 0 auto 96px;
}

.womanBlock {

  background: linear-gradient(to bottom, rgba(235, 244, 253, 1) 0%, rgba(237, 245, 253, 1) 100%);
  padding: 38px calc(14% - 47px) 34px calc(14% - 47px);

  margin-bottom: 96px;

  position: relative;

  z-index: 1;


  &__img {

    display: block;
    max-width: 805px;
    width: 100%;
    position: absolute;
    left: 100px;
    bottom: 50px;

    z-index: 2;
  }

  &__titleBlock {

    margin-bottom: 32px;
    padding-left: calc(100% / 2.7);

    position: relative;
    left: 100px;

    &-title {
      font-size: 70px;
      line-height: 1;
      font-weight: 700;
      margin-bottom: 15px;

      span {
        color: #30B5DF;
      }
    }

    p {
      max-width: 450px;
      font-size: 17px;
      line-height: 1.5;
    }
  }

  &__cards {

    display: flex;
    justify-content: space-between;
    gap: 16px;

    position: relative;

    z-index: 3;


    &-list {

      li {
        position: relative;
        margin-bottom: 24px;
      }

      li:last-child {
        margin-bottom: 55px;
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

    &-item {
      display: flex;
      justify-content: space-between;

      background-color: rgba(#fff, .96);
      border-radius: 16px;
      padding: 32px;

      width: 100%;


      &:first-child {
        img {
          max-width: 171px;
          align-self: start;
        }
      }

      &:last-child {
        img {
          max-width: 145px;
          align-self: start;
        }
      }

      &--title {
        color: #0B1F35;
        font-weight: 700;
        margin-bottom: 24px;
      }
    }

  }
}


</style>