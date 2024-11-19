<script setup>
import {onMounted, onUnmounted, ref} from "vue";

import Header from '@/components/Header.vue';
import Hero from "@/components/Hero.vue";
import Specializations from "@/components/Specializations.vue";
import ThreeCardsSlider from "@/components/ThreeCardsSlider/ThreeCardsSlider.vue";
import TheCalculator from "@/components/Calculator/TheCalculator.vue";
import LoveBlock from "@/components/LoveBlock.vue";
import TheCommand from "@/components/TheCommand.vue";
import PremiumBlock from "@/components/PremiumBlock.vue";
import StoriesBlock from "@/components/StoriesBlock.vue";
import FormVisitBlock from "@/components/FormVisitBlock.vue";
import SuspicionBlock from "@/components/SuspicionBlock.vue";
import WomanBlock from "@/components/WomanBlock.vue";
import CareSliderBlock from "@/components/CareSliderBlock.vue";
import PatientsSayBlock from "@/components/PatientsSayBlock.vue";
import TagsBlock from "@/components/TagsBlock.vue";
import PopularQuestionsBlock from "@/components/PopularQuestionsBlock.vue";
import Accordion from "@/components/Accordion/Accordion.vue";
import MoreDetailsBlock from "@/components/MoreDetailsBlock.vue";
import Footer from "@/components/Footer.vue";
import CopyRigthing from "@/components/CopyRigthing.vue";

const width = ref(document.documentElement.clientWidth)

const onResize = () => width.value = document.documentElement.clientWidth;

onMounted(() => {
  window.addEventListener('resize', onResize);
})

onUnmounted(() => {
  window.removeEventListener('resize', onResize);
})

</script>

<template>

  <div class="container">

    <Header :width='width' :onResize="onResize"/>

    <main>

      <Hero :width='width' :onResize="onResize"/>

      <Specializations/>

      <ThreeCardsSlider/>

      <TheCalculator :width='width' :onResize="onResize"/>

<!--            <LoveBlock/>-->

<!--            <TheCommand/>-->

      <!--      <PremiumBlock/>-->

      <!--      <StoriesBlock/>-->

      <!--      <FormVisitBlock/>-->

      <!--      <SuspicionBlock/>-->

    </main>

  </div>

  <!--  <WomanBlock/>-->

  <!--  <div class="container">-->

  <!--    <CareSliderBlock/>-->

  <!--    <PatientsSayBlock/>-->

  <!--    <TagsBlock/>-->

  <!--    <PopularQuestionsBlock/>-->

  <!--    <Accordion/>-->

  <!--    <MoreDetailsBlock/>-->

  <!--  </div>-->

  <!--  <div class="horizontalLine"></div>-->

  <!--  <div class="container">-->

  <!--    <Footer/>-->

  <!--  </div>-->

  <!--  <div class="horizontalLine second"></div>-->

  <!--  <div class="container">-->

  <!--    <CopyRigthing/>-->

  <!--  </div>-->

</template>

<style lang="scss">
@import "@/assets/scss/variables";

.container {
  max-width: $desc-width;
  //padding-left: calc(11% - 45px);
  //padding-right: calc(11% - 45px);
  margin: 0 auto;

  @include _1170 {
    padding: 0 24px 0;
  }

  @include _660 {
    padding: 0 8px 0;
  }
}

.horizontalLine {
  background-color: #D1D6DB;
  height: 1px;
  margin-bottom: 64px;
}

.horizontalLine.second {
  margin-bottom: 20px;
}

</style>


