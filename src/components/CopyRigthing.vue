<script setup>

</script>

<template>
  <div class="copyRighting">
    <div class="copyRighting__work">
      Работаем с 2016 г.
    </div>
    <div class="copyRighting__materials">
      Материалы с сайта защищены законом РФ об авторских и смежных правах. Копирование запрещено.<br> Сайт не является
      договором офферты
    </div>
    <div class="copyRighting__politics">
      <a href="#">Политика конфенденциальности</a>
    </div>
  </div>
</template>


<style scoped lang="scss">
.copyRighting {

  display: flex;
  justify-content: space-between;
  padding-bottom: 20px;

  &__work {
    font-size: 12px;
    font-weight: 400;
    color: #4D5761;
  }

  &__materials {
    font-size: 12px;
    color: #111C27;
    text-align: center;
  }

  &__politics {
    font-size: 12px;

    a {
      color: #111C27;
    }

  }
}
</style>