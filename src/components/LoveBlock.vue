<script setup>

</script>

<template>
  <div class="loveBlock">
    <div class="loveBlock__text">
      <div class="loveBlock__text-title">
        Ami Clinic создана <span>с любовью</span>
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


  &__text {

    &-title {
      font-size: 50px;
      font-weight: 700;
      color: #111C27;
      letter-spacing: -0.5px;
      margin-bottom: 16px;

      span {
        color: $primary-color;
      }
    }

    p {
      font-size: 17px;
      line-height: 1.5;
      color: #384450;
      max-width: 560px;
    }

    p:first-of-type {
      margin-bottom: 16px;
    }

    p:last-of-type {
      margin-bottom: 48px;
    }
  }

  &__img {
    img {
      display: block;
      max-width: 518px;
    }
  }

  &__text-cards {
    display: flex;
    justify-content: space-between;
    max-width: 78%;

    &-item--title {
      font-size: 35px;
      font-weight: 700;
      line-height: 1.15;
      color: #111C27;
    }

    &-item--descr {
      font-size: 15px;
      line-height: 1.4;
      color: #384150;
    }

  }

}

</style>