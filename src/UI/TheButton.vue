<script setup>

defineProps({
  isBluBtn: Boolean,
  isGreenBtn: Boolean,
  isTransparentBtn: Boolean,
  isSpecBtn: Boolean,
  isCalcBtn: Boolean,
  isManagementBtn: Boolean,
  isCommandBtn: Boolean,
  isCommandCardsBtn: Boolean,
  isStoriesSliderBtb: Boolean,
  isSuspicionBtb: Boolean,
  isCareSlider: Boolean
})

</script>


<template>

  <button :class="{
    button: true,
    blueHeroBtn: isBluBtn,
    greenHeroBtn: isGreenBtn,
    transparentHeroBth: isTransparentBtn,
    specBtn: isSpecBtn,
    calculatorBtn: isCalcBtn,
    managementBtn: isManagementBtn,
    commandBtn: isCommandBtn,
    commandCardsBtn: isCommandCardsBtn,
    storiesSliderBtb: isStoriesSliderBtb,
    suspicionBtb: isSuspicionBtb,
    careSliderBtn: isCareSlider

  }">
    <slot></slot>
  </button>

</template>


<style scoped lang="scss">

@import "../assets/scss/variables";

.button {
  outline: none;
  border: none;
  cursor: pointer;
  background-color: transparent;
}

.blueHeroBtn {
  padding: 18px 24px;
  background-color: $primary-color;
  border-radius: 8px;
  color: $white;
  font-size: 15px;
  line-height: 130%;
  font-weight: 500;

  transition: background-color .2s linear;

  &:hover {
    background-color: darken($primary-color, 5);
  }
}

.greenHeroBtn {
  padding: 18px 24px;
  background-color: #25D366;
  border-radius: 8px;
  color: $white;
  font-size: 15px;
  line-height: 130%;
  font-weight: 500;

  transition: background-color .2s linear;

  &:hover {
    background-color: darken(#25D366, 5);
  }
}

.transparentHeroBth {

  position: relative;

  background-color: rgba(#fff, 50%);
  border-radius: 8.6px;

  padding: 22px 26px;

  img {
    display: block;
  }

  @include _660 {
    padding: 18px 14px;
  }

}

.specBtn {
  background-color: $primary-color;
  color: $white;
  font-size: 15px;
  line-height: 1.3;
  font-weight: 500;
  padding: 18px 24px;
  border-radius: 8px;
}

.calculatorBtn {
  width: 100%;
  padding: 23px 0;
  border-radius: 10px;
  border: 1px solid #E5E7EB;
  transition: .2s linear;

  &:active {
    border: 1px solid #30B5DF;
    background-color: rgba(#30B5DF1A, 10%);
    color: #30B5DF;
    transition: .2s linear;
  }
}

.managementBtn {
  font-size: 15px;
  color: #111C27;
  font-weight: 500;
  border: 1px solid #D1D6DB;
  border-radius: 8px;
  padding: 8px 14px;

  transition: .15s linear;

  &:hover {
    color: $white;
    background-color: $primary-color;
    border-color: $primary-color;
  }
}

.commandBtn {
  font-size: 17px;
  color: #111827;
  font-weight: 500;
  line-height: 1.41;
  background-color: #F3F4F6;
  border-radius: 60px;
  padding: 8px 20px;

  transition: .15s linear;

  &:hover {
    background-color: $primary-color;
    color: $white;
  }
}

.commandCardsBtn {
  font-size: 15px;
  line-height: 1.5;
  font-weight: 500;
  color: #fff;
  background-color: $primary-color;
  border-radius: 8px;
  width: 100%;
  padding: 18px 54px;
  margin-bottom: 16px;
  max-width: 260px;
}

.storiesSliderBtb {

  padding: 8px 14px 8px 14px;
  color: #888D93;
  border: 1px solid rgba(#D1D6DB, .5);
  border-radius: 8px;
  cursor: pointer;

  z-index: 10;

  transition: border .2s linear, color .2s linear;

  &:hover {
    border: 1px solid #D1D6DB;
    color: #111C27;
  }
}

.suspicionBtb {
  padding: 18px 24px;
  background-color: #FFFFFF;
  border: 1px solid #D1D6DB;
  border-radius: 8px;
  color: #111827;
  font-size: 15px;
  font-weight: 500;

  transition: background-color .2s linear;

  &:hover {
    background-color: rgba(#D1D6DB, 0.2);
  }
}

.careSliderBtn {
  color: #111C27;
  font-size: 15px;
  padding: 8px 14px;
  border: 1px solid #D1D6DB;
  border-radius: 8px;

  transition: background-color .2s linear;

  &:hover {
    background-color: rgba(#D1D6DB, 0.2);
  }
}

</style>