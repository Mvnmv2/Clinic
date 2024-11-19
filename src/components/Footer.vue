<script setup>

import TheButton from '../UI/TheButton.vue'
import TheTag from '@/UI/TheTag.vue'

</script>

<template>
  <div class="footer">
    <div class="footer__left">
      <div class="footer__left-titleBlock">
        <img src="../assets/images/logoFooter.png" alt="logoFooter">
        <div class="footer__left-titleBlock-text">
          Заботливая стоматология,<br>
          которую вы полюбите.
        </div>
      </div>

      <div class="footer__left-form">
        <form action="#">
          <input type="tel" placeholder="Введите номер телефона">
          <TheButton :isBluBtn="true">Записаться</TheButton>
          <div class="footer__left-form_checkBlock">
            <input type="checkbox">
            <label>Нажимая кнопку вы соглашаетесь с условиями<br><a href="#">политики конфиденциальности</a>.</label>
          </div>
        </form>
      </div>

      <ul class="footer__left-contacts">
        <li>
          <img src="../assets/images/clockIcon.svg" alt="clockIcon">
          <p>Пн-Вс 9:00-21:00</p>
        </li>
        <li>
          <img src="../assets/images/LocationIcon.svg" alt="LocationIcon">
          <p>г. Москва, ул. Таганская, д. 26, стр. 1</p>
        </li>
      </ul>

      <ul class="footer__left-icons">
        <li>
          <img src="../assets/images/vk.svg" alt="vk">
        </li>
        <li>
          <img src="../assets/images/ok.svg" alt="ok">
        </li>
        <li>
          <img src="../assets/images/youtube.svg" alt="youtube">
        </li>
      </ul>

    </div>
    <div class="footer__right">

      <ul class="footer__right-list">
        <li class="footer__right-list__title">Клиника</li>
        <li class="footer__right-list__item">О нас</li>
        <li class="footer__right-list__item">Врачи</li>
        <li class="footer__right-list__item">Отзывы<TheTag :heroBlock="true">157</TheTag></li>
        <li class="footer__right-list__item">Акции, рассрочка</li>
        <li class="footer__right-list__item">Статьи</li>
        <li class="footer__right-list__item">Контакты</li>
      </ul>

      <ul class="footer__right-list">
        <li class="footer__right-list__title">Услуги</li>
        <li class="footer__right-list__item">All-on-4 / Имплантация</li>
        <li class="footer__right-list__item">Лечение зубов / Терапия</li>
        <li class="footer__right-list__item">Выравнивание зубов / Ортопедия</li>
        <li class="footer__right-list__item">Эстетика/Ортопедия</li>
        <li class="footer__right-list__item">Зуботехническая лаборатория</li>
        <li class="footer__right-list__item">Рассчёт стоимости онлайн</li>
      </ul>

      <ul class="footer__right-list">
        <li class="footer__right-list__title">Телефон</li>
        <li class="footer__right-list__item">+7 8125 000 00 00</li>
        <li class="footer__right-list__title">Отвечаем онлайн</li>
        <li class="footer__right-list__item">WhatsApp</li>
        <li class="footer__right-list__item">Viber</li>
        <li class="footer__right-list__item">Telegram</li>
      </ul>

      <ul class="footer__right-list">
        <li class="footer__right-list__title">Преимущества</li>
        <li class="footer__right-list__item">Лечение без боли и стресса</li>
        <li class="footer__right-list__item">Собственная зуботехническая лаборатория</li>
        <li class="footer__right-list__item">Полное восстановление зубов за 1 день</li>
        <li class="footer__right-list__item">Бесплатный первичный прием</li>
        <li class="footer__right-list__item">Рассрочка от клиники</li>
        <li class="footer__right-list__item">Все врачи работают с оптикой — увеличиение до 40 крат</li>
      </ul>
    </div>
  </div>

</template>

<style scoped lang="scss">

.footer {
  @import "../assets/scss/variables";

  display: grid;
  grid-template-columns: 1fr 1.5fr;
  column-gap: 17px;
  margin-bottom: 40px;

  &__left {

    &-titleBlock {
      display: flex;
      align-items: center;
      margin-bottom: 32px;

      img {
        display: block;
        max-width: 146px;
        margin-right: 20px;
      }

      &-text {
        font-size: 14px;
        font-weight: 500;
        line-height: 130%;
        border-left: 1px solid #4D5561;
        padding-left: 20px;
      }
    }

    &-form {
      margin-bottom: 32px;

      input {
        padding: 18px 35px;
        margin-right: 4px;
        border: 1px solid #949DA6;
        border-radius: 10px;
        outline: none;

        font-size: 15px;
        color: $black-color;

        &::placeholder {
          font-size: 15px;
          color: #949DA6;
        }
      }

      &_checkBlock {
        margin: 24px 0 32px;

        label {
          font-size: 14px;
          color: #111827;

          a {
            color: #111827;
            text-decoration: underline;
            margin-left: 18px;
          }

        }
      }
    }

    &-contacts {
      li {
        display: flex;
        column-gap: 12px;
        margin-bottom: 16px;
      }

    }

    &-icons {
      display: flex;
    }
  }

  &__right {

    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    column-gap: 78.5px;
    row-gap: 56px;

    &-list {
      &__title {
        color: #111C27;
        font-size: 15px;
        line-height: 1;
        font-weight: 600;

        margin-bottom: 20px;
      }

      &__item {
        color: #111C27;
        font-size: 15px;
        line-height: 1;
        font-weight: 400;
        margin-bottom: 20px;
      }

      &__item:last-child {
        margin-bottom: 0;
      }
    }

    &-list:last-child {
      grid-column: 1 / span 3;
    }
  }
}

</style>