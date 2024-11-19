<script setup>

const data = [
  {
    "id": 1,
    "question": "Правда ли, что имплантация all-on-4 подходит не всем?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  },
  {
    "id": 2,
    "question": "Действительно ли можно сразу есть твердую пищу?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  },
  {
    "id": 3,
    "question": "Если имплант не приживётся (отторгнется)?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  },
  {
    "id": 4,
    "question": "Из чего формируется цена All-on-4?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  },
  {
    "id": 5,
    "question": "All-on-4 действительно делается за один день?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  }
  ,
  {
    "id": 6,
    "question": "Требуется ли костная пластика при имплантации на 4-х имплантах?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  }
  ,
  {
    "id": 7,
    "question": "Чем отличаются импланты разных производителей?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  }
  ,
  {
    "id": 8,
    "question": "Кому противопоказана имплантация по протоколу All-on-4?",
    "answer": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
    "isOpen": false
  }
]

import AccordionItem from "@/components/Accordion/AccordionItem.vue";
import {ref} from "vue";

const toggleAnswer = id => {
  faqs.value = faqs.value.map(faq => faq.isOpen && faq.id !== id ? {...faq, isOpen: false} : faq)
  faqs.value = faqs.value.map(faq => faq.id === id ? {...faq, isOpen: !faq.isOpen} : faq)
}

const faqs = ref(data)

</script>

<template>

  <div class="accordionBlock">

    <AccordionItem v-for="faq in faqs"
                   :key="faq.id"
                   :faq="faq"
                   @toggle-answer="toggleAnswer"/>
  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables.scss";

.accordionBlock {

  display: flex;
  flex-wrap: wrap;

  column-gap: 48px;
  align-items: center;
  margin-bottom: 96px;
}

</style>