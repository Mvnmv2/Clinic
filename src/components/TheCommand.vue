<script setup>
import {reactive, ref} from 'vue'
import TheButton from '@/UI/TheButton.vue'
import 'vue3-carousel/dist/carousel.css'
import {Carousel, Slide, Pagination, Navigation} from 'vue3-carousel'


const currentSlide = ref(0)

const slides =  [
  {
    item1: {
      image: 'src/assets/images/comand/comand1.png',
      name: 'Попов Константин Юрьевич',
      profession1: 'Челюстно-лицевой хирург,',
      profession2: 'стоматолог-хирург',
      experience: '10 лет'
    },
    item2: {
      image: 'src/assets/images/comand/comand2.png',
      name: 'Дремалов Борис Михайлович',
      profession1: 'Челюстно-лицевой хирург,',
      experience1: '15 лет, кандидат',
      experience2: ' медицинских наук'
    },
    item3: {
      image: 'src/assets/images/comand/comand3.png',
      name: 'Гаджиев Юсуп Исламович',
      profession1: 'Челюстно-лицевой хирург,',
      experience1: '15 лет, кандидат',
      experience2: ' медицинских наук'

    },
  },

  {
    item1: {
      image: 'src/assets/images/comand/comand1.png',
      name: 'Иванов Сергей Петрович',
      profession1: 'Челюстно-лицевой хирург,',
      profession2: 'стоматолог-хирург',
      experience: '10 лет'
    },
    item2: {
      image: 'src/assets/images/comand/comand2.png',
      name: 'Михайлов Павел Сергеевич',
      profession1: 'Челюстно-лицевой хирург,',
      experience1: '15 лет, кандидат',
      experience2: ' медицинских наук'
    },
    item3: {
      image: 'src/assets/images/comand/comand3.png',
      name: 'Кучумов Михаил Павлович',
      profession1: 'Челюстно-лицевой хирург,',
      experience1: '15 лет, кандидат',
      experience2: ' медицинских наук'
    },
  },

]



</script>

<template>

  <div class="command__title">Ami Команда</div>
  <div class="command__subTitle">Познакомьтесь с теми, кто вложит высокий стандарт Ami Clinic<br>
    <span>в вашу новую улыбку</span></div>
  <div class="command__buttons">
    <TheButton :isCommandBtn="true">Хирурги</TheButton>
    <TheButton :isCommandBtn="true">Ортопеды</TheButton>
    <TheButton :isCommandBtn="true">Техники</TheButton>
    <TheButton :isCommandBtn="true">Терапевты</TheButton>
    <TheButton :isCommandBtn="true">Ассистенты</TheButton>
    <TheButton :isCommandBtn="true">Кураторы</TheButton>
  </div>
  <div class="command__slider">

    <div class="command__slider-buttons">
      <carousel :items-to-show="1" v-model="currentSlide">

        <slide v-for="{item1, item2, item3} in slides" :key="item1">
          <ul class="command__slider-cards">
            <li class="command__slider-cards--item">
              <img :src="item1.image" alt="стоматолог1">
              <div class="name-wrapper">
                <div class="name">{{ item1.name }}</div>
                <div class="profession">
                  {{ item1.profession1 }}
                  <br>
                  {{ item1.profession2 }}
                </div>
                <div class="experience">
                  Стаж: <span>{{ item1.experience }}</span>
                </div>
                <div class="buttonsBlock">
                  <TheButton :isCommandCardsBtn="true">Записаться на приём</TheButton>
                  <a class="profession-popup" href="#">Подробнее о враче</a>
                </div>
              </div>
            </li>
            <li class="command__slider-cards--item">
              <img :src="item2.image" alt="стоматолог2">
              <div class="name-wrapper">
                <div class="name">{{ item2.name }}</div>
                <div class="profession">
                  {{ item2.profession1 }}
                </div>
                <div class="experience">
                  Стаж: <span>{{ item2.experience1 }}<br>
          {{ item2.experience2 }}</span>
                </div>
                <div class="buttonsBlock">
                  <TheButton :isCommandCardsBtn="true">Записаться на приём</TheButton>
                  <a class="profession-popup" href="#">Подробнее о враче</a>
                </div>
              </div>
            </li>
            <li class="command__slider-cards--item">
              <img :src="item3.image" alt="стоматолог3">
              <div class="name-wrapper">
                <div class="name">{{ item3.name }}</div>
                <div class="profession">
                  {{ item3.profession1 }}
                </div>
                <div class="experience">
                  Стаж:
                  <span>{{ item3.experience1 }}<br>{{ item3.experience2 }}</span>
                </div>
                <div class="buttonsBlock">
                  <TheButton :isCommandCardsBtn="true">Записаться на приём</TheButton>
                  <a class="profession-popup" href="#">Подробнее о враче</a>
                </div>
              </div>
            </li>
          </ul>
        </slide>

        <template #addons>
          <!--          <navigation/>-->
          <div>
            <button @click="next">Next</button>
            <input type="number" min="0" max="9" v-model="currentSlide"/>
            <button @click="prev">Prev</button>
          </div>
          <pagination/>
        </template>
      </carousel>
    </div>
  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.command__title {
  font-size: 67px;
  line-height: 1.25;
  font-weight: 700;
  color: #111C27;
  margin-bottom: 16px;
  text-align: center;
}

.command__subTitle {
  font-size: 20px;
  color: #111C27;
  margin-bottom: 32px;
  text-align: center;

  span {
    color: #16A3D0;
  }
}

.command__buttons {
  display: flex;
  gap: 8px;
  justify-content: center;
  margin-bottom: 40px;
}

.command__slider {
  margin-bottom: 64px;
}

.command__slider-cards {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-bottom: 16px;

  &--item {

    border: 1px solid #D1D5DB;
    border-radius: 20px;
    text-align: center;

    img {
      max-width: 328px;
      display: flex;
      margin-bottom: 24px;
    }

    .name-wrapper {
      display: inline-block;

      margin: 0 auto;

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

      span {
        font-weight: 600;
      }
    }

    .buttonsBlock {
      display: flex;
      align-items: start;
      flex-direction: column;
      margin-bottom: 32px;

      .profession-popup {
        display: inline-block;
        color: inherit;
        margin: 0 auto;

        &:visited {
          color: #4D5561;
        }
      }
    }
  }
}


</style>