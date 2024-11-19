<script setup>
import TheButton from '@/UI/TheButton.vue';
import TheTag from '@/UI/TheTag.vue'

defineProps({
  width: Number,
})

</script>

<template>

  <div class="hero">

    <div class="slider-card_1">
      <img v-if="width > 770" class="hero-img" src="../assets/images/hero-img.png" alt="hero-img">
      <img v-else-if="width > 476" class="hero-img_tablet" src="../assets/images/hero-img_tablet.png"
           alt="hero-img_900">
      <img v-else class="hero-img_mob" src="../assets/images/hero-img_mobile.png" alt="hero-img_900">

      <div class="title">

        <div class="sup-title">
          Cтоматология
        </div>

        <div class="sub-title">
          <img src="../assets/images/amcl.svg" alt="amclinic title">
        </div>
        <div class="sub-sub-title">
          Заботливая стоматология, которую вы полюбите!
        </div>

        <div class="buttons-block">
          <TheButton :is-blu-btn="true">Запись на первый приём</TheButton>
          <TheButton :is-green-btn="true">Узнать стоимость WhatsApp</TheButton>
        </div>

        <div class="info-block">
          <div class="visit-time">
            <img src="../assets/images/clockIcon.svg" alt="clock">
            <div class="visit-info">
              Пн-Вс 9:00-21:00
            </div>
          </div>
          <div class="address">
            <img src="../assets/images/locationIcon.svg" alt="location">
            <div class="address-info">
              г. Москва, ул. Таганская, д. 26, стр. 1
            </div>
          </div>
        </div>
      </div>

      <div class="buttons-block-second">

        <div class="buttons-block-second__btn">
          <TheButton class="btn1" :isTransparentBtn="true">
            <img src="../assets/images/zoonpng.png" alt="zoon"> <!--:style="{maxWidth: '63px'}"-->
            <TheTag :heroBlock="true">60</TheTag>
          </TheButton>

          <TheButton class="btn2" :isTransparentBtn="true">
            <img  src="../assets/images/prodoctorov.png" alt="prodoctorov">
            <!--:style="{maxWidth: '138px'}"-->
            <TheTag :heroBlock="true">34</TheTag>
          </TheButton>
          <TheButton class="btn3" :isTransparentBtn="true">
            <img  src="../assets/images/otzovic.png" alt="otzovic"> <!--:style="{maxWidth: '116px'}"-->
            <TheTag :heroBlock="true">4</TheTag>
          </TheButton>
        </div>
      </div>
    </div>
  </div>

</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.hero {

  &-img {
    margin: 0 auto;
    display: block;
    max-width: 1130px;
    width: 100%;

    &_tablet {
      max-width: 720px;
      width: 100%;
    }

    &_mob {
      //max-width: 360px;
      width: 100%;
    }
  }
}

.slider-card_1 {
  position: relative;

  @include _660 {
    display: flex;
    flex-direction: column;
    align-items: center;

    width: 100%;
  }
}

.title {

  position: absolute;
  left: 5%;
  top: 29%;

  @media (max-width: 930px) {
    top: 50%;
    transform: translateY(-50%);
  }

  @include _660 {
    width: 100%;
    height: 100%;

    padding: 32px 0 100px 0;

    display: flex;
    flex-direction: column;
    align-items: center;

    left: 0;

  }

}

.sup-title {
  font-size: 25px;
  font-weight: 500;
  color: #4D5561;
  margin-bottom: 16px;

  @include _660 {
    font-size: 14px;
  }
}

.sub-title {

  @include _660 {
    img {
      width: 100%;
      max-width: 200px;
    }
  }
}

.sub-sub-title {
  font-size: 15px;
  color: #111C27;
  line-height: 90%;
  font-weight: 400;
  margin-bottom: 24px;

  @include _660 {
    max-width: 200px;
    margin-bottom: auto;
    text-align: center;
  }
}

.buttons-block {
  display: flex;
  gap: 8px;
  margin-bottom: 23px;

  @include _660 {
    flex-direction: column;
    margin-bottom: 0;
  }
}

.info-block {
  display: grid;
  grid-template-columns: .5fr 1fr;

  @include _660 {
    display: none;
  }
}

.visit-time, .address {
  display: flex;
  gap: 12px;
  align-items: center;
}

.visit-info, .address-info {
  font-size: 15px;
  color: #111C27;
}

.buttons-block-second__btn {
  display: flex;
  gap: 8px;
  position: absolute;
  right: 32px;
  bottom: 32px;

  @include _1100 {
    display: none;
  }

  @include _660 {
    display: flex;
    bottom: 16px;
    right: 50%;
    transform: translateX(50%);
  }

  .btn1 {

    img {
      max-width: 63px;

      @include _660 {
        max-width: 43px;
      }
    }
  }

  .btn2 {
    img {
      max-width: 138px;

      @include _660 {
        max-width: 94px;
      }
    }
  }

  .btn3 {

    img {
      max-width: 116px;

      @include _660 {
        max-width: 80px;
      }
    }
  }

}


</style>