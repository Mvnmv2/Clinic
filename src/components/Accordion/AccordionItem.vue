<script setup>

defineProps(['faq'])

const emit = defineEmits(['toggleAnswer'])
const handleClick = id => emit('toggleAnswer', id)

</script>

<template>

  <div class="accordionBlock__item" @click="() => handleClick(faq.id)">

    <div class="accordionBlock__item-title" >
      <p> {{ faq.question }}</p>
      <img :style="{ display: faq.isOpen ? 'none' : 'block'}" src="../../assets/images/PlusButton.svg" alt="PlusButton">
      <img :style="{ display: faq.isOpen ? 'block' : 'none'}" src="../../assets/images/MinusButton.svg" alt="MinusButton">
    </div>
    <div class="accordionBlock__item-content" :class="['answer', {active: faq.isOpen}]">{{ faq.answer }}</div>
  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables.scss";

.accordionBlock__item {

  width: calc(50% - 24px);

  &-title {
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;

    font-size: 17px;
    line-height: 130%;
    font-weight: 500;
    color: $black-color;

    height: 50px;
  }

  &-content {
    font-size: 15px;
    line-height: 150%;
    font-weight: 400;
    color: #6B7280;

    height: 0;
    overflow-y: auto;
    transition: height .5s;
  }

  border-bottom: 1px solid #D1D5DB;
}

.active {
  height: 110px;
}

.show {
  display: block;
}

</style>