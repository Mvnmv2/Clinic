<script setup>
import TheButton from '../UI/TheButton.vue'
</script>

<template>
  <div class="container">
    <ul class="cardList">
      <li class="card-item"><img src="../assets/images/specs/spec1.jpg" alt="card image">
        <div class="card-item__block">
          <div class="title">
            All-on-4 / Имплантация
          </div>
          <div class="subTitle">
            Полное восстановление зубов за 1 день
          </div>
          <TheButton :is-spec-btn="true">Узнать подробнее</TheButton>
        </div>
      </li>
      <li class="card-item"><img src="../assets/images/specs/spec2.jpg" alt="card image">
        <div class="card-item__block">
          <div class="title">
            Лечение зубов
          </div>
          <div class="subTitle">
            Терапия
          </div>
          <TheButton :is-spec-btn="true">Узнать подробнее</TheButton>
        </div>
      </li>
      <li class="card-item"><img src="../assets/images/specs/spec3.jpg" alt="card image">
        <div class="card-item__block">
          <div class="title">
            Выравнивание зубов
          </div>
          <div class="subTitle">
            Ортодонтия
          </div>
          <TheButton :is-spec-btn="true">Узнать подробнее</TheButton>
        </div>
      </li>
      <li class="card-item"><img src="../assets/images/specs/spec4.jpg" alt="card image">
        <div class="card-item__block">
          <div class="title">
            Эстетика/виниры
          </div>
          <div class="subTitle">
            Ортопедия
          </div>
          <TheButton :is-spec-btn="true">Узнать подробнее</TheButton>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.container {
  padding: 16px 0 32px;
}

.cardList {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 8px;

  @include _900 {
    grid-template-columns: 1fr;
  }
}

.card-item {
  position: relative;

  img {
    display: block;
    max-width: 100%;

    object-fit: cover;
    border-radius: 16px;

    @include _900 {
      min-height: 268px;
    }
  }

  &__block {
    position: absolute;
    left: 32px;
    bottom: 32px;
    color: $white;

    @include _900 {
      left: 16px;
      bottom: 24px;
    }


    .title {
      position: static;
      font-size: 20px;
      font-weight: 500;
      margin-bottom: 8px;
    }

    .subTitle {
      position: static;
      font-size: 15px;
      margin-bottom: 16px;
      max-width: 232px;
    }
  }

}
</style>