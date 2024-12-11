<script setup>
import TheButton from '@/UI/TheButton.vue'

const props = defineProps({
  slide: Object
})

</script>

<template>

      <div class="command__slider-cards--item">
        <img :src="props.slide.image" alt="стоматолог">
        <div class="name-wrapper">
          <div class="name">{{ props.slide.name }}</div>
          <div class="profession">
            {{ props.slide.profession }}
          </div>
          <div class="experience">
            Стаж: <span>{{ props.slide.experience }}</span>
          </div>
          <div class="buttonsBlock">
            <TheButton :isCommandCardsBtn="true">Записаться на приём</TheButton>
            <a class="profession-popup" href="#">Подробнее о враче</a>
          </div>
        </div>
      </div>




</template>

<style scoped lang="scss">

  .command__slider-cards--item {

    display: flex;
    flex-direction: column;

    border: 1px solid #D1D5DB;
    border-radius: 20px;
    text-align: center;

    img {
      width: 100%;
      max-width: 100%;
      display: block;
    }

    .name-wrapper {
      display: flex;
      flex-direction: column;

      padding: 24px 35px 32px 35px;

      flex-basis: 289px;

      .name {
        color: #000;
        font-size: 17px;
        line-height: 1.5;
        font-weight: 600;
        text-align: left;

      }

      .profession {
        font-size: 15px;
        line-height: 1.5;
        font-weight: 400;
        color: #384450;
        margin-bottom: 24px;
        text-align: left;

      }
    }

    .experience {
      font-size: 15px;
      line-height: 1.5;
      color: #384450;
      margin-bottom: 24px;
      text-align: left;

      flex: 1;

      span {
        font-weight: 600;
      }
    }

    .buttonsBlock {
      display: flex;
      flex-direction: column;
      align-items: center;

      .profession-popup {
        display: inline-block;
        color: inherit;

        &:visited {
          color: #4D5561;
        }
      }
    }
  }


</style>