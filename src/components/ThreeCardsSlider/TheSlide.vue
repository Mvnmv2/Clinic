<script setup>

defineProps({
  title: String,
  description: String,
  img: String
})

</script>

<template>

  <div class="card-item">
    <div class="content">
      <div class="content-description">
        <div class="content-description__title">
          {{title}}
        </div>
        <div class="content-description__subTitle">
          {{description}}
        </div>
      </div>
      <div class="content-img">
        <img :src="img" alt="card-img">
      </div>
    </div>
  </div>

</template>

<style lang="scss" scoped>

.card-item {
  background-color: #F7F9FC;
  border-radius: 20px;
  padding: 40px 32px 0 32px;

}

.content {

  &-img {

    img {
      display: block;
      max-width: 163px;
      width: 100%;
    }
  }
}

.content-description {

  &__title {
    color: #111827;
    font-size: 20px;
    line-height: 1.2;
    font-weight: 500;
    margin-bottom: 24px;

  }

  &__subTitle {
    color: #384450;
    font-size: 15px;
    line-height: 1.3;
    margin-bottom: 54px;




  }
}

</style>