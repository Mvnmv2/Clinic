<script setup>

</script>

<template>
  <div class="tagsBlock">
    <div class="tagsBlock__title">
      Придя к нам однажды — приходят после <span>всей семьёй</span>
    </div>
    <ul class="tagsBlock__card">
      <li class="tagsBlock__card_Item">
        <img class="tagsBlock__card_Item-imgTag" src="../assets/images/tagsBlock/Tag1.svg" alt="Tag1">
        <img class="tagsBlock__card_Item-img" src="../assets/images/tagsBlock/img1.svg" alt="zoon">
      </li>
      <li class="tagsBlock__card_Item">
        <img class="tagsBlock__card_Item-imgTag" src="../assets/images/tagsBlock/Tag2.svg" alt="Tag2">
        <img class="tagsBlock__card_Item-img" src="../assets/images/tagsBlock/img2.svg" alt="продокторов">
      </li>
      <li class="tagsBlock__card_Item">
        <img class="tagsBlock__card_Item-imgTag" src="../assets/images/tagsBlock/Tag3.svg" alt="Tag3">
        <img class="tagsBlock__card_Item-img" src="../assets/images/tagsBlock/img3.svg" alt="отзовик">
      </li>
    </ul>
  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.tagsBlock {
  max-width: 938px;
  margin: 0 auto 96px;
  text-align: center;
  font-weight: 500;

  &__title {
    font-size: 32px;
    color: #384450;
    margin-bottom: 32px;

    span {
      color: $primary-color;
    }
  }

  &__card {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 186px;

    justify-content: center;

    &_Item {
      display: flex;
      align-items: center;
      justify-content: center;

      position: relative;

      &:first-child img:first-child {
        right: 18%;
      }

      &:nth-child(2) img:first-child {
        right: 0;
      }

      &:nth-child(3) img:first-child {
        right: 5%;
      }

      &-imgTag {
        top: 18%;
        position: absolute;
      }
    }
  }
}

</style>