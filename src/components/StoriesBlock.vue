<script setup>
import TheButton from '../UI/TheButton.vue';

</script>

<template>
  <h2 class="stories-title">Даже в тех случаях, <span>где другие клиники бессильны</span></h2>
  <h3 class="stories-sup__title">Реальные истории пациентов</h3>

  <ul class="stories__buttons-list">
    <li class="stories__buttons-list_item">
      <TheButton :isCommandBtn="true">Все</TheButton>
    </li>
    <li class="stories__buttons-list_item">
      <TheButton :isCommandBtn="true">All-on-4</TheButton>
    </li>
    <li class="stories__buttons-list_item">
      <TheButton :isCommandBtn="true">Лечение зубов</TheButton>
    </li>
    <li class="stories__buttons-list_item">
      <TheButton :isCommandBtn="true">Ортодонтия</TheButton>
    </li>
    <li class="stories__buttons-list_item">
      <TheButton :isCommandBtn="true">Ортопедия</TheButton>
    </li>
  </ul>

  <div class="stories-slider">
    <div class="stories-slider__card">
      <div class="stories-slider__card-left">
        <img src="../assets/images/stories/1.jpeg" alt="card photo">
      </div>
      <div class="stories-slider__card-right">
        <div class="stories-slider__card-right__title">Лечение переодонтида</div>
        <div class="stories-slider__card-right__subtitle">Врачи</div>
        <p class="stories-slider__card-right__description">Гаджиев Юсуп Исламович, Гаджиев Юсуп Исламович,<br>
          Гаджиев Юсуп Исламович</p>
        <div class="stories-slider__card-right__subtitle">C чем обратились</div>
        <p class="stories-slider__card-right__description">Lorem Ipsum is simply dummy text of the printing and
          typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an
          unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
        <div class="stories-slider__card-right__subtitle">C чем обратились</div>
        <p class="stories-slider__card-right__description">Lorem Ipsum is simply dummy text of the printing and
          typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an
          unknown printer took a galley of type and scrambled it to make a type specimen book.</p>

        <div class="stories-slider__card-right__price-block">
          <div class="stories-slider__card-right__price-block__price">
            <p>Стоимость</p>
            <p>250 000 руб.</p>
          </div>
          <div class="stories-slider__card-right__price-block__time">
            <p>Сроки</p>
            <p>1 день</p>
          </div>
        </div>
      </div>
    </div>

    <div class="stories-slider__menage-block">
      <div class="stories-slider__menage-block_pagination">
        1 из 20
      </div>
      <div class="stories-slider__menage-block_buttons">
        <TheButton :isStoriesSliderBtb="true">Назад</TheButton>
        <TheButton :isStoriesSliderBtb="true">Далее</TheButton>
      </div>
    </div>
  </div>

</template>

<style scoped lang="scss">

.stories-title {
  font-size: 42px;
  font-weight: 700;
  color: #111C27;
  margin-bottom: 20px;

  span {
    color: #16A3D0;
  }
}

.stories-sup__title {
  font-size: 20px;
  color: #111C27;
  line-height: 120%;
  margin-bottom: 32px;
}

.stories__buttons-list {
  display: flex;
  gap: 8px;
  margin-bottom: 40px;
}

.stories-slider {

  max-height: 558px;
  margin-bottom: 110px;

  &__card {
    display: flex;
    column-gap: 8px;
    padding-bottom: 40px;


    &-left {
      img {
        max-width: 439px;
        display: block;
      }
    }

    &-right {
      display: flex;
      flex-direction: column;
      justify-content: center;
      width: 100%;
      padding-left: 56px;
      padding-right: 48px;
      border: 1px solid #D1D5DB;
      border-radius: 20px;
      background-color: #F9FAFB;
      color: #111C27;

      &__title {
        font-size: 24px;
        font-weight: 500;
        margin-bottom: 32px;
      }

      &__subtitle {
        font-size: 17px;
        font-weight: 500;
        margin-bottom: 12px;
      }

      &__description {
        font-size: 15px;
        line-height: 150%;
        font-weight: 400;
        margin-bottom: 24px;
      }


      &__price-block {
        display: flex;
        column-gap: 24px;

        &__price, &__time {
          p:first-child {
            font-weight: 900;
            margin-bottom: 12px;
          }
        }
      }
    }
  }

  &__menage-block {
    display: flex;
    justify-content: space-between;
    margin-bottom: 110px;

    &_pagination {
      color: #6B7680;
    }

    &_buttons {
      display: flex;
      column-gap: 12px;
    }
  }

}
</style>