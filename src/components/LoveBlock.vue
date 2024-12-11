<script setup>

defineProps({
  width: Number,
})

</script>

<template>
  <div class="loveBlock">
    <div class="loveBlock__text">
      <div class="loveBlock__text-title">
        Ami Clinic<br v-if="width < 901" > создана <span>с любовью</span>
      </div>
      <p>В 2016 году я привез технологию All-on-4 в Россию,
        сделав ставку на инновацию. Мне говорили: “Ничего не получится!”
        “Технология не подходит для российских реалий”
        Но у меня была вера и твердое убеждение:
        All-on-4 — это шанс получить новые зубы.
        Как свои, только еще лучше. </p>
      <p>Я понимаю, насколько сейчас трудно выбрать стоматологию.
        На рынке сотни предложений “Зубы за 1 день”.
        Но мы видим огромное количество ошибок — когда присылают слепки, снимки, непроверенные окклюзии. Ведь еще 5 лет
        назад 9 из 10 врачей отрицали саму возможность такой операции. </p>

      <ul class="loveBlock__text-cards">
        <li class="loveBlock__text-cards-item">
          <div class="loveBlock__text-cards-item--title">
            с 2016г
          </div>
          <div class="loveBlock__text-cards-item--descr">
            Работаем по<br>технологии All-on-4
          </div>
        </li>
        <li class="loveBlock__text-cards-item">
          <div class="loveBlock__text-cards-item--title">
            35 000+
          </div>
          <div class="loveBlock__text-cards-item--descr">
            Установленных<br>имплантов
          </div>
        </li>
        <li class="loveBlock__text-cards-item">
          <div class="loveBlock__text-cards-item--title">
            6000+
          </div>
          <div class="loveBlock__text-cards-item--descr">
            Восстановленно<br>челюстей
          </div>
        </li>
      </ul>
    </div>
    <div class="loveBlock__img">
      <img src="../assets/images/loveBlock.png" alt="loveBlock image">
    </div>
  </div>
</template>

<style scoped lang="scss">

.loveBlock {
  @import "@/assets/scss/variables";
  display: flex;
  align-items: center;
  margin-bottom: 67px;

  @include _900 {
    flex-direction: column;
  }


  &__text {

    @include _900 {
      padding: 0 110px;
    }

    @include _768 {
      padding: 0 25px;
    }

    &-title {
      font-size: 50px;
      font-weight: 700;
      color: #111C27;
      letter-spacing: -0.5px;
      margin-bottom: 16px;

      span {
        color: $primary-color;
      }

      @include _768 {
        font-size: 43px;
        text-align: center;
      }
    }

    p {
      font-size: 17px;
      line-height: 1.5;
      color: #384450;
      max-width: 560px;

      @include _900 {
        max-width: 100%;
      }
    }

    p:first-of-type {
      margin-bottom: 16px;
    }

    p:last-of-type {
      margin-bottom: 48px;

      @include _768 {
        margin-bottom: 40px;
      }
    }
  }

  &__img {

    @include _900 {
      order: -1;
    }

    img {
      display: block;
      max-width: 518px;

      @include _900 {
        max-width: 488px;
      }

      @include _768 {
        max-width: 345px;
      }
    }
  }

  &__text-cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    max-width: 78%;

    @include _900 {
      row-gap: 32px;
      max-width: 100%;
    }

    &-item--title {
      font-size: 35px;
      font-weight: 700;
      line-height: 1.15;
      color: #111C27;

      @include _768 {
        font-size: 33px;
      }
    }

    &-item--descr {
      font-size: 15px;
      line-height: 1.4;
      color: #384150;
    }

  }

}

</style>