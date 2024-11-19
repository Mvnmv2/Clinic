<script setup>
import TheButton from '../UI/TheButton.vue'
import {ref, computed} from "vue";

const items = ref([
  {
    id: 1,
    img: 'src/assets/images/moreDetails/1.png',
    title: 'Цифровое протезирование зубов: история пациента',
    description: 'Каждый пациент мечтает об идеально точном, красивом и качественном результате.',
    moreText: `Corporis, cumque dicta doloremque dolorum eaque esse excepturi, exercitationem facilis hic id iusto laborum nemo
        numquam porro praesentium ut vel. Aut iusto minus molestias obcaecati odit placeat sit suscipit veniam!`

  },
  {
    id: 2,
    img: 'src/assets/images/moreDetails/2.png',
    title: 'Цифровое протезирование зубов: история пациента',
    description: 'Каждый пациент мечтает об идеально точном, красивом и качественном результате.',
    moreText: `Aperiam architecto cum delectus dolore doloribus ea id illum labore maiores, minus obcaecati optio possimus quam
    quia, quis saepe sapiente suscipit tempore vel vitae. Est exercitationem iste non repudiandae rerum.`

  },
  {
    id: 3,
    img: 'src/assets/images/moreDetails/3.png',
    title: 'Цифровое протезирование зубов: история пациента',
    description: 'Каждый пациент мечтает об идеально точном, красивом и качественном результате.',
    moreText: `Eius incidunt porro quae quia unde! Ab accusantium beatae deleniti deserunt dolor dolores doloribus earum enim
    est eveniet facilis illum in iure nostrum quam quidem quos tempora, totam ut veritatis?`

  }
])

</script>

<template>
  <div class="MoreDetailsBlock">
    <div class="MoreDetailsBlock__title">
      <div class="MoreDetailsBlock__title-text">
        Подробнее об All-on-4 в нашем блоге
      </div>
      <TheButton :isCareSlider="true">Cмотреть все</TheButton>
    </div>

    <ul class="MoreDetailsBlock__list">
      <li v-for="item of items" key="item.id">
        <img :src="item.img" alt="image">
        <p class="MoreDetailsBlock__list-title">{{ item.title }}</p>
        <p class="MoreDetailsBlock__list-text">{{ item.description }}</p>
        <div class="MoreDetailsBlock__list-more">
          <img src="../assets/images/Icon.svg" alt="Icon">
          <a href="#">Читать подробнее</a>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";

.MoreDetailsBlock {

  margin-bottom: 64px;

  &__title {

    display: flex;
    justify-content: space-between;
    margin-bottom: 32px;

    &-text {
      font-size: 32px;
      font-weight: 500;
      line-height: 125%;
      color: $black-color;
    }
  }

  &__list {
    display: flex;
    flex-wrap: wrap;
    column-gap: 25px;

    img {
      display: block;
      max-width: 360px;
      margin-bottom: 17px;
    }

    &-title {
      font-size: 20px;
      font-weight: 700;
      line-height: 120%;
      color: #000;
      margin-bottom: 8px;
    }

    &-text {
      font-size: 15px;
      font-weight: 400;
      line-height: 150%;
      color: $black-color;
      margin-bottom: 32px;
    }

    &-more {
      display: flex;
      column-gap: 8px;

      a {
        line-height: 1;
        color: #6B7280;
      }

      img {
        display: block;
      }
    }
  }
}

</style>