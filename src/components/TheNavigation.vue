<script setup>
import TheTag from '@/UI/TheTag.vue'
import {ref} from "vue";

defineProps({
  burger: Boolean
})

const openBurger = ref(false)

function onClick() {
  openBurger.value = true
}

function closeBurger() {
  openBurger.value = false
}

</script>

<template>
  <nav class="nav">

    <div
        :class="['burger__openBtn', burger ? 'burger__openBtn-open' : '']"
        @click="onClick"
        >Меню<span></span>
    </div>

    <ul :class="['nav-list', burger ? 'burger' : '',
    openBurger ? 'burger-open' : 'burger-close']"
    >

      <li class="burger__closeBtn" @click="closeBurger">&#10005;</li>

      <li class="nav-item">
        <a class="nav-link" href="#">
          Услуги
          <svg width="9.500000" height="5.500000" viewBox="0 0 9.5 5.5" fill="none" xmlns="http://www.w3.org/2000/svg">
            <defs/>
            <path id="Icon"
                  d="M9.28 0.21C9.57 0.51 9.57 0.98 9.28 1.28L5.28 5.28C4.98 5.57 4.51 5.57 4.21 5.28L0.21 1.28C-0.08 0.98 -0.08 0.51 0.21 0.21C0.51 -0.08 0.98 -0.08 1.28 0.21L4.75 3.68L8.21 0.21C8.51 -0.08 8.98 -0.08 9.28 0.21Z"
                  fill-opacity="1.000000" fill-rule="evenodd"/>
          </svg>
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">
          О&nbsp;клинике
          <svg width="9.500000" height="5.500000" viewBox="0 0 9.5 5.5" fill="none" xmlns="http://www.w3.org/2000/svg"
          >
            <defs/>
            <path id="Icon"
                  d="M9.28 0.21C9.57 0.51 9.57 0.98 9.28 1.28L5.28 5.28C4.98 5.57 4.51 5.57 4.21 5.28L0.21 1.28C-0.08 0.98 -0.08 0.51 0.21 0.21C0.51 -0.08 0.98 -0.08 1.28 0.21L4.75 3.68L8.21 0.21C8.51 -0.08 8.98 -0.08 9.28 0.21Z"
                  fill-opacity="1.000000" fill-rule="evenodd"/>
          </svg>
        </a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">
          Отзывы
          <TheTag class="tag">157</TheTag>
        </a>
      </li>
      <li class="nav-item"><a class="nav-link" href="#">Акции,&nbsp;рассрочки</a></li>
      <li class="nav-item">
        <a class="nav-link" href="#">
          Статьи
        </a>
      </li>
      <li class="nav-item"><a class="nav-link" href="#">Контакты</a></li>
    </ul>


  </nav>
</template>

<style lang="scss" scoped>
@import "@/assets/scss/variables";

.nav {

  width: 100%;
  position: relative;

  &-list {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: space-between;
    max-width: 700px;

    @include _900 {
      display: none;
    }

    @include _1170 {
      max-width: 100%;
    }

    .burger__closeBtn {
      position: absolute;
      right: 10%;
      top: 5%;

      font-weight: 600;
      color: #FFFFFF;
      cursor: pointer;
    }

  }

  &-link {
    color: #384450;
    transition: .1s linear;

    svg {
      fill: #000000;
    }
  }

  &-link:hover {
    color: darken(#384450, 30);
  }

  &-item {
    font-size: 17px;
  }

  &-link {
    svg {
      margin-left: 8px;
      height: 8px;
    }
  }

  &-item:nth-child(4) {

    .nav-link {
      position: relative;

      .tag {
        position: absolute;
        left: 150%;
        top: -50%;

        @include _900 {
          background-color: #fff;
          color: #16A3D0;
        }
      }
    }

  }
}

.nav-list.burger {
  display: flex;
  flex-direction: column;

  transition: .2s linear;

  transform: translateX(100%);
  visibility: hidden;


  position: absolute;
  z-index: 2;
  top: 5px;
  right: 24px;

  background-color: #30B5DF;
  border-radius: 8px;
  padding: 20px;

  @include _660 {
    right: 8px;
  }

  .nav-link {
    color: #fff;

    svg {
      fill: #FFFFFF;
      margin-bottom: 1px;
    }
  }

  &.burger-open {
    transform: translateX(0);
    visibility: visible;

  }

  &.burger-close {
    transform: translateX(100%);
    visibility: hidden;
  }

}

.burger__openBtn {

  font-size: 15px;
  line-height: 150%;
  color: #30B5DF;
  cursor: pointer;

  display: none;

  column-gap: 10px;
  align-items: center;
  justify-content: end;

  &-open {
    display: flex;
  }

  span {

    position: relative;

    display: inline-block;
    width: 21px;
    height: 2px;
    background-color: #30B5DF;
    border-radius: 20px;


    &:before, &:after {
      content: "";
      width: 21px;
      height: 2px;
      background-color: #30B5DF;
      border-radius: 20px;

    }

    &:before {
      position: absolute;
      top: -6px;
      left: 0;
    }

    &:after {
      position: absolute;
      top: 6px;
      left: 0;
    }
  }
}

</style>