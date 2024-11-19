<script setup>

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

.premium-title {
  color: #16A3D0;
  text-align: center;
  margin-bottom: 22px;
  font-size: 50px;
  font-weight: 700;

  span {
    color: #111C27;
  }
}

.premium-card {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 1fr);
  gap: 8px;

  margin-bottom: 125px;

  &__item {

    img {
      display: block;
      width: 100%;
      max-height: 278px;
    }

    &:nth-child(1) {
      grid-column: 1 / span 2;
      grid-row: 1 / 2;
    }

    &:nth-child(6) {
      grid-column: 3 / span 2;
      grid-row: 2 / 3;
    }
  }
}


</style>