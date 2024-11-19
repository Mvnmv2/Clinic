<script setup>
import TheButton from '../UI/TheButton.vue'
</script>

<template>
  <div class="popularQuestion">
    <div class="popularQuestion__card">
      <img class="popularQuestion__card-img" src="../assets/images/popularBlockImg.png" alt="img card"/>
      <div class="popularQuestion__card-description">
        <div class="popularQuestion__card-description-title">
          Популярные вопросы
        </div>
        <p>
          Здравствуйте!<br>
          Меня зовут Ирина, я ваш куратор лечения.<br>
          Собрала для вас ответы на частые вопросы по All-on-4.<br>
          По любым другим буду рада проинструктировать вас лично,<br>
          Время ответа до 10 минут.
        </p>
        <TheButton :isGreenBtn="true">Задать вопрос WhatsApp</TheButton>
      </div>
    </div>

  </div>
</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.popularQuestion {

  margin-bottom: 40px;

  &__card {
    display: flex;
    column-gap: 56px;

    padding: 24px;
    background-color: #F9FAFB;
    border-radius: 40px;

    &-img {
      max-width: 328px;
    }

    &-description {
      &-title {
        font-size: 32px;
        font-weight: 500;
        line-height: 125%;
        color: $black-color;
        margin-bottom: 24px;
      }

      p {
        font-size: 17px;
        line-height: 150%;
        color: #384450;
        margin-bottom: 24px;
      }
    }
  }
}

</style>