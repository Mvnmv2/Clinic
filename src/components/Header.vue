<script setup>
import TheNavigation from "@/components/TheNavigation.vue";

defineProps({
  width: Number,
})

</script>

<template>
  <header class="header">

    <div class="logo">
      <a href="#"><img src="@/assets/images/logo.svg" alt="logo" class="logo"></a>
      <div class="line"></div>
      <div class="logo-description">
        Заботливая стоматология,<br>которую вы полюбите.
      </div>
    </div>

    <TheNavigation :burger="width < 900"/>

  </header>
</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.header {

  padding: 25px 0;
  background-color: $white;

  display: flex;
  gap: 7%;
  align-items: center;

  @include _1170 {
    gap: 3%;
  }

  @include _768 {
    padding: 9px 0;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 20px;

    .line {
      width: 1px;
      height: 43px;
      background-color: #4D5561;

      @include _1170 {
        display: none;
      }
    }

    &-description {
      color: #4D5561;
      font-size: 14px;
      min-width: 185px;

      @include _1170 {
        display: none;
      }
    }

    img {
      display: block;
      max-width: 146px;
      height: auto;

      @include _1170 {
        max-width: 133px;
      }
    }
  }
}

</style>