<script setup>
import TheButton from '../UI/TheButton.vue';

defineProps({
  width: Number,
})

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
        <img v-if="width > 1100" src="../assets/images/stories/1.jpeg" alt="card photo">
        <img v-else src="../assets/images/stories/3.jpeg" alt="card photo">
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
@import "@/assets/scss/variables.scss";

.stories-title {
  font-size: 42px;
  font-weight: 700;
  color: #111C27;
  margin-bottom: 20px;

  span {
    color: #16A3D0;
  }

  @include _1100 {
    font-size: 32px;
    margin-bottom: 16px;
  }
}

.stories-sup__title {
  font-size: 20px;
  color: #111C27;
  line-height: 120%;
  margin-bottom: 32px;

  @include _1100 {
    font-size: 14px;
    margin-bottom: 24px;
  }
}

.stories__buttons-list {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 40px;

  @include _1100 {
    margin-bottom: 24px;
  }
}

.stories-slider {

  max-height: 558px;
  margin-bottom: 210px;

  @include _1100 {
    max-height: none;
    margin-bottom: 110px;
  }

  @include _768 {
    margin-bottom: 80px;
  }

  @include _660 {
    margin-bottom: 49px;
  }

  &__card {
    display: flex;
    column-gap: 8px;
    padding-bottom: 40px;

    @include _1100 {
      flex-direction: column;
      row-gap: 8px;
      padding-bottom: 20px;

    }

    &-left {
      img {
        width: 100%;
        display: block;
      }
    }

    &-right {
      display: flex;
      flex-direction: column;
      justify-content: center;
      width: 100%;
      padding: 15px 48px 15px 56px;
      border: 1px solid #D1D5DB;
      border-radius: 20px;
      background-color: #F9FAFB;
      color: #111C27;

      @include _1100 {
        padding-top: 64px;
        padding-bottom: 77px;

      }

      @include _660 {
        padding: 40px 24px;
      }

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
    align-items: center;


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