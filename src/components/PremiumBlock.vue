<script setup>

defineProps({
  width: Number,
})

</script>

<template>
  <h2 class="premium-title">Премиальный уровень комфорта <span>на 350 м²</span></h2>
  <div class="premium-card">
    <div class="premium-card__item">
      <img src="../assets/images/premiumBlock/1.jpeg" alt="card-1">
    </div>
    <div class="premium-card__item">
      <img src="../assets/images/premiumBlock/2.jpeg" alt="card-2">
    </div>
    <div class="premium-card__item">
      <img src="../assets/images/premiumBlock/3.jpeg" alt="card-3">
    </div>
    <div class="premium-card__item">
      <img src="../assets/images/premiumBlock/4.jpeg" alt="card-4">
    </div>
    <div class="premium-card__item">
      <img src="../assets/images/premiumBlock/5.jpeg" alt="card-5">
    </div>
    <div class="premium-card__item">
      <img src="../assets/images/premiumBlock/6.jpeg" alt="card-6">
    </div>
  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";


.premium-title {
  color: #16A3D0;
  text-align: center;
  margin-bottom: 22px;
  font-size: 50px;
  font-weight: 700;

  span {
    color: #111C27;
  }

  @include _768 {
    font-size: 38px;
  }
}

.premium-card {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 1fr);
  gap: 8px;

  margin-bottom: 120px;

  @include _768 {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);

    margin-bottom: 70px;
  }

  @include _360 {
    margin-bottom: 56px;
  }

  &__item {

    img {
      display: block;
      width: 100%;
      height: 100%;
      max-height: 278px;
      border-radius: 16px;

      @include _768 {
        max-height: 245px;
        border-radius: 8px;
        object-fit: cover;
      }
    }

    &:nth-child(1) {
      grid-column: 1 / span 2;
      grid-row: 1 / span 1;

      @include _768 {
        grid-column: 1 / span 1;
        grid-row: 1 / span 1;

        img {
          height: 100%;
        }
      }
    }

    &:nth-child(6) {
      grid-column: 3 / span 2;
      grid-row: 2 / 3;

      @include _768 {
        grid-column: 1 / span 1;
        grid-row: 3 / span 1;

        img {
          height: 100%;

        }
      }
    }
  }
}


</style>