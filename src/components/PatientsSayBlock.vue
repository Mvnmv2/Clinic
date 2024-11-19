<script setup>
import TheButton from '../UI/TheButton.vue'
</script>

<template>
  <div class="patientsSayBlock__title">
    Пациенты говорят
  </div>
  <div class="patientsSayBlock__subTitle">
    “Спасибо судьбе, что привела в Ami Clinic”
  </div>

  <div class="patientsSayBlock__slider">
    <div class="patientsSayBlock__slider-card">
      <div class="patientsSayBlock__slider-card-item">
        <div class="patientsSayBlock__slider-card-item_left">
          <div class="patientsSayBlock__slider-card-item_left-title">
            В другой клинике мне не смогли предложить<br> <span>одномоментную имплантацию</span>
          </div>
          <div class="patientsSayBlock__slider-card-item_left-description">
            У меня проблемы с зубами с 15 лет. С 15 лет мне попадались непонятные стоматологи, которые угробили мне все
            зубы верхней челюсти. Последний стоматолог, к которому я попала, поставил мне мосты с металлокерамическими
            коронками, которые начали отваливаться через 3 дня. И в конечном итоге я осталась без всех верхних зубов
            верхней челюсти, остались одни корни. Я начала следующего стоматолога, который бы надо мной поиздевался. Он
            сделал, я проходила с этими коронками, мостами 13 лет. А сейчас герметичность нарушилась и эти мосты у меня
            упали. Я сделала панорамный снимок и у меня приговор - я лишаюсь всех зубов верхней челюсти. Начала искать,
            что делать. Прочитала весь интернет...
          </div>
          <div class="reedMoreBtn">
            <img src="../assets/images/Icon.svg" alt="Icon">
            Читать полностью
          </div>
        </div>
        <div class="patientsSayBlock__slider-card-item_right">
          <div class="patientsSayBlock__slider-card-item_right-imgBlock">
            <img src="../assets/images/girl.jpeg" alt="girl">
            <div class="patientsSayBlock__slider-card-item_right-imgBlock-name">Колчина Елизавета</div>
          </div>
          <div class="patientsSayBlock__slider-card-item_right-player">
            <img src="../assets/images/Player.svg" alt="Player">
          </div>
        </div>
      </div>
      <div class="patientsSayBlock__slider-card-item">
        <div class="patientsSayBlock__slider-card-item_left">
          <div class="patientsSayBlock__slider-card-item_left-title">
            В другой клинике мне не смогли предложить<br> <span>одномоментную имплантацию</span>
          </div>
          <div class="patientsSayBlock__slider-card-item_left-description">
            У меня проблемы с зубами с 15 лет. С 15 лет мне попадались непонятные стоматологи, которые угробили мне все
            зубы верхней челюсти. Последний стоматолог, к которому я попала, поставил мне мосты с металлокерамическими
            коронками, которые начали отваливаться через 3 дня. И в конечном итоге я осталась без всех верхних зубов
            верхней челюсти, остались одни корни. Я начала следующего стоматолога, который бы надо мной поиздевался. Он
            сделал, я проходила с этими коронками, мостами 13 лет. А сейчас герметичность нарушилась и эти мосты у меня
            упали. Я сделала панорамный снимок и у меня приговор - я лишаюсь всех зубов верхней челюсти. Начала искать,
            что делать. Прочитала весь интернет...
          </div>
          <div class="reedMoreBtn">
            <img src="../assets/images/Icon.svg" alt="Icon">
            Читать полностью
          </div>
        </div>
        <div class="patientsSayBlock__slider-card-item_right">
          <div class="patientsSayBlock__slider-card-item_right-imgBlock">
            <img src="../assets/images/girl.jpeg" alt="girl">
            <div class="patientsSayBlock__slider-card-item_right-imgBlock-name">Колчина Елизавета</div>
          </div>
          <div class="patientsSayBlock__slider-card-item_right-player">
            <img src="../assets/images/Player.svg" alt="Player">
          </div>
        </div>
      </div>

    </div>
    <div class="patientsSayBlock__slider-menage">
      <div class="patientsSayBlock__slider-menage_pagination">
        2 из 3
      </div>
      <div class="patientsSayBlock__slider-menage_buttons">
        <TheButton :isCareSlider="true">Назад</TheButton>
        <TheButton :isCareSlider="true">Далее</TheButton>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/scss/variables";

.patientsSayBlock {

  &__title {
    color: #16A3D0;
    font-weight: 500;
    line-height: 125%;
    font-size: 32px;
    margin-bottom: 24px;
    text-align: center;
  }

  &__subTitle {
    color: $black-color;
    font-weight: 600;
    line-height: 115%;
    font-size: 40px;
    margin-bottom: 18px;
    text-align: center;
  }

  &__slider {

    padding: 0 96px 0 96px;

    margin-bottom: 40px;

    &-card {

      &-item {
        display: flex;
        justify-content: space-between;
        padding-top: 38px;
        padding-bottom: 32px;
        border-bottom: 1px solid #D1D6DB;

        &_left {
          &-title {
            font-size: 22px;
            color: $black-color;
            font-weight: 600;
            margin-bottom: 32px;

            span {
              color: $primary-color;
            }
          }

          &-description {
            font-size: 15px;
            line-height: 150%;
            color: $black-color;
            max-width: 555px;
            margin-bottom: 24px;
          }
        }

        &_right {

          background-color: #F3F5F6;
          padding: 12px 12px 16px;
          border-radius: 28px;

          &-imgBlock {
            position: relative;
            display: inline-block;

            img {
              display: block;
              max-width: 273px;
              border-radius: 16px;
            }

            &-name {
              font-size: 15px;
              line-height: 150%;
              color: #FFFFFF;
              position: absolute;
              right: 16px;
              bottom: 16px;
              z-index: 2;
            }
          }

          &-player {
            margin-top: 16px;
          }
        }
      }
    }

    &-menage {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 16px;

      &_pagination {
        font-size: 15px;
        line-height: 20px;
        color: #6B7680;
      }

      &_buttons {
        display: flex;
        column-gap: 12px;
      }
    }
  }
}

.reedMoreBtn {
  color: #4D5761;
  font-size: 15px;
  line-height: 141%;
  cursor: pointer;

  img {
    display: inline-block;
    margin-right: 5px;
  }
}

</style>