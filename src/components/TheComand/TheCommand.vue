<script setup>
import {Swiper, SwiperSlide} from 'swiper/vue';
import {Navigation} from 'swiper/modules';
import {reactive, ref} from 'vue'
import TheButton from '@/UI/TheButton.vue'

import 'vue3-carousel/dist/carousel.css'

import {register} from 'swiper/element/bundle';
import Slide from "@/components/TheComand/Slide.vue";

register();

const currentSlide = ref(0)

// const slides = [
//   {
//     item1: {
//       image: 'src/assets/images/comand/comand1.png',
//       name: 'Попов Константин Юрьевич',
//       profession1: 'Челюстно-лицевой хирург,',
//       profession2: 'стоматолог-хирург',
//       experience: '10 лет'
//     },
//     item2: {
//       image: 'src/assets/images/comand/comand2.png',
//       name: 'Дремалов Борис Михайлович',
//       profession1: 'Челюстно-лицевой хирург,',
//       experience1: '15 лет, кандидат',
//       experience2: ' медицинских наук'
//     },
//     item3: {
//       image: 'src/assets/images/comand/comand3.png',
//       name: 'Гаджиев Юсуп Исламович',
//       profession1: 'Челюстно-лицевой хирург,',
//       experience1: '15 лет, кандидат',
//       experience2: ' медицинских наук'
//
//     },
//   },
//
//   {
//     item1: {
//       image: 'src/assets/images/comand/comand1.png',
//       name: 'Иванов Сергей Петрович',
//       profession1: 'Челюстно-лицевой хирург,',
//       profession2: 'стоматолог-хирург',
//       experience: '10 лет'
//     },
//     item2: {
//       image: 'src/assets/images/comand/comand2.png',
//       name: 'Михайлов Павел Сергеевич',
//       profession1: 'Челюстно-лицевой хирург,',
//       experience1: '15 лет, кандидат',
//       experience2: ' медицинских наук'
//     },
//     item3: {
//       image: 'src/assets/images/comand/comand3.png',
//       name: 'Кучумов Михаил Павлович',
//       profession1: 'Челюстно-лицевой хирург,',
//       experience1: '15 лет, кандидат',
//       experience2: ' медицинских наук'
//     },
//   },
//
// ]

const slides = [
  {
    image: 'src/assets/images/comand/comand1.png',
    name: 'Попов Константин Юрьевич',
    profession: 'Челюстно-лицевой хирург, стоматолог-хирург',
    experience: '10 лет'
  },
  {
    image: 'src/assets/images/comand/comand2.png',
    name: 'Дремалов Борис Михайлович',
    profession: 'Челюстно-лицевой хирург',
    experience: '15 лет, кандидат медицинских наук',
  },
  {
    image: 'src/assets/images/comand/comand3.png',
    name: 'Гаджиев Юсуп Исламович',
    profession: 'Челюстно-лицевой хирург',
    experience: '15 лет, кандидат медицинских наук',
  },
  {
    image: 'src/assets/images/comand/comand1.png',
    name: 'Иванов Сергей Петрович',
    profession: 'Челюстно-лицевой хирург',
    profession2: 'стоматолог-хирург',
    experience: '10 лет'
  },
  {
    image: 'src/assets/images/comand/comand2.png',
    name: 'Михайлов Павел Сергеевич',
    profession: 'Челюстно-лицевой хирург',
    experience: '15 лет, кандидат медицинских наук',
  },
  {
    image: 'src/assets/images/comand/comand3.png',
    name: 'Кучумов Михаил Павлович',
    profession: 'Челюстно-лицевой хирург',
    experience: '15 лет, кандидат медицинских наук',
  }

]


</script>

<template>

  <div class="command__container">

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

    <swiper-container
        class="swiper-container"
        :slides-per-view="3"
        :space-between="10"
        :breakpoints="{
          // when window width is >= 320px
          320: {
          slidesPerView: 1
          },
          480: {
          slidesPerView: 2
          },
          1100: {
          slidesPerView: 3
          }}"
        :navigation="{
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
          }"
        :pagination="{
         el: '.pagination',
        }"

    >
      <swiper-slide v-for="(slide, index) in slides" :key="index">
        <Slide :slide="slide"/>
      </swiper-slide>

    </swiper-container>

    <div class="swiper-pagination"></div>

    <div class="command__menage-block">
      <div class="command__menage-block_pagination pagination">
        1 из 20
      </div>
      <div class="command__menage-block_buttons">
        <TheButton class="swiper-button-prev" :isStoriesSliderBtb="true">Назад</TheButton>
        <TheButton class="swiper-button-next" :isStoriesSliderBtb="true">Далее</TheButton>
      </div>
    </div>
  </div>


</template>

<style scoped lang="scss">
@import "@/assets/scss/variables.scss";

.command__container {
  margin-bottom: 64px;
}

.swiper-container {
  margin-bottom: 28px;
}

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
  flex-wrap: wrap;
  gap: 8px;
  justify-content: center;
  margin-bottom: 40px;
}


.command__menage-block {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 110px;

  &_pagination {
    color: #6B7680;
  }

  &_buttons {
    display: flex;
    column-gap: 12px;
  }
}


</style>