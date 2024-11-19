<script setup>

import TheButton from '../UI/TheButton.vue'
</script>


<template>
  <div class="formVisit">
    <img class="doctor-imd" src="../assets/images/doctor.png" alt="doctor image">
    <div class="formVisitBlock">
      <div class="formVisitBlock__title">
        <span>Один визит</span> приблизит<br>
        вас к решению проблемы.
      </div>
      <div class="formVisitBlock__subTitle">
        Запишитесь на комплексный приём чтобы узнать:
      </div>
      <ul class="formVisitBlock__list">
        <li>Возможно ли восстановить зубы за 1 день в вашем случае</li>
        <li>Какие импланты и метод имплантации подойдут вам 100%</li>
        <li>Стоимость имплантации "под ключ" + план лечения</li>
      </ul>

      <form class="formVisitBlock__form">
        <input type="tel" placeholder="Введите номер телефона">
        <TheButton :isBluBtn="true">Записаться</TheButton>
      </form>

      <div class="formVisitBlock__gift">
        <div class="formVisitBlock__gift--left">
          <img src="../assets/images/gift.png" alt="gift">
          <p>Первый приём<br>абсолютно бесплатный </p>
        </div>
        <div class="formVisitBlock__gift--right">
          <img src="../assets/images/gift.png" alt="gift">
          <p>КТ обеих челюстей<br>
            в подарок</p>
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped lang="scss">

.formVisit {
  position: relative;
}

.doctor-imd {
  display: block;
  max-width: 550px;
  position: absolute;
  z-index: 5;
  right: 0;
  bottom: 0;
}

.formVisitBlock {
  background-color: #F9FAFB;
  padding: 80px 0 64px 80px;
  border-radius: 24px;

  margin-bottom: 104px;

  &__title {

    color: #111827;
    font-size: 36px;
    line-height: 1;
    font-weight: 700;
    margin-bottom: 16px;

    span {
      color: #30B5DF;
    }
  }

  &__subTitle {
    font-size: 17px;
    font-weight: 500;
    margin-bottom: 20px;
  }

  &__list {


    padding-left: 16px;

    li {
      position: relative;
      margin-bottom: 20px;
      font-size: 15px;
      //line-height: 1.5;
    }

    li:last-child {
      margin-bottom: 24px;
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

  &__form {
    display: flex;
    column-gap: 4px;
    margin-bottom: 24px;
  }

  input {
    width: 100%;
    max-width: 248px;
    border: 1px solid #949DA6;
    border-radius: 10px;
    outline: none;
    padding-left: 35px;
  }

  &__gift {
    display: flex;
    column-gap: 45px;

    &--right, &--left {
      display: flex;
      align-items: center;
      column-gap: 4px;
    }

    img {
      display: block;
      width: 54px;
    }

  }

}

</style>