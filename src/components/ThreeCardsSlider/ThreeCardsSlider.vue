<script setup>
import {register} from 'swiper/element/bundle';

register();

import {Swiper, SwiperSlide} from 'swiper/vue';
import TheSlide from './TheSlide.vue'

import 'swiper/scss';

const slideData = [
  {
    id: 1,
    title: "Лечение у специалистов\n" + "с 20-ти летнем опытом.",
    description: '500+ отзывов на независимых ресурсах а так же видео отзывы и отзывы с результатами у нас на сайте.',
    img: 'src/assets/images/cardBlock/1.png'
  },
  {
    id: 2,
    title: "Оптимальное решение\n" + "под ваш бюджет",
    description: 'Озвученная на приёме стоимость окончательная. Вам не придётся доплачивать ни за какие доп.услуги или материалы в процессе',
    img: 'src/assets/images/cardBlock/2.png'
  },
  {
    id: 3,
    title: "Вы полностью контролируете\n" + "процесс",
    description: 'Личный куратор на связи 24/7: отвечает на ваши вопросы понятным языком и «ведет за руку» по плану лечения.',
    img: 'src/assets/images/cardBlock/3.png'
  }
]

</script>

<template>

  <div class="slider-container">
    <swiper-container
        class="swiper"
        slides-per-view="3"
        space-between="16"
        :breakpoints="{
    300: {
      slidesPerView: 1,
      spaceBetween: 200,
    },
      540: {
        slidesPerView: 2,
      },
      1080: {
        slidesPerView: 3,
  },
    }"
    >
      <swiper-slide v-for="(slide, index) in slideData">
        <TheSlide class="slide"
                  :title="slide.title"
                  :description="slide.description"
                  :img="slide.img"
                  :key="slide.id"
        />
      </swiper-slide>
    </swiper-container>

  </div>
</template>

<style scoped lang="scss">
@import "@/assets/scss/variables.scss";

.slider-container {

  margin-bottom: 96px;

  display: flex;

  @include _768 {
    margin-bottom: 72px;
  }

  @include _360 {
    margin-bottom: 52px;
  }

  width: 100%;
  overflow: hidden;
}


.swiper {
  width: 100%;

  .slide {
    width: 100%;
    height: 100%;

  }
}

</style>






