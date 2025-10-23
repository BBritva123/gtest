<template>
  <div class="services">
    <div class="container">
      <h3 class="sevices__header">
        <a
          href="#"
          aria-label="Переход по ссылке для получения списка медицинских услуг"
        >
          Все медицинские услуги Гемотест
          <span class="count__services">(35)</span>
          <span class="icon__services">→</span>
        </a>
      </h3>
      <ul class="services__card-list card-list">
        <li class="services__card-item">
          <img
            src="/img/fns.svg"
            alt="Справка"
            class="card-list__img"
            loading="lazy"
          />
          <h4 class="card-list__head">
            <span class="card-list__head--color">
              Справка в налоговую (ФНС)
            </span>
            для оформления налогового вычета
          </h4>
        </li>
        <li class="services__card-item">
          <img
            src="/img/consultant.svg"
            alt="консультация"
            class="card-list__img"
            loading="lazy"
          />
          <h4 class="card-list__head">
            <span class="card-list__head--color">Бесплатная консультация</span>
            врача Гемотест по телефону
          </h4>
        </li>
        <li class="services__card-item">
          <img
            src="/img/decode.svg"
            alt="результат"
            class="card-list__img"
            loading="lazy"
          />
          <h4 class="card-list__head">
            <span class="card-list__head--color">Расшифровка результатов</span>
            из других лабораторий
          </h4>
        </li>
        <li class="services__card-item">
          <img
            src="/img/discount.svg"
            alt="Бонусы"
            class="card-list__img"
            loading="lazy"
          />
          <h4 class="card-list__head">
            <span class="card-list__head--color">Бонусная программа</span>
            «Копите на здоровье»
          </h4>
        </li>
        <li class="services__card-item">
          <img
            src="/img/cancer.svg"
            alt="Экспертиза"
            class="card-list__img"
            loading="lazy"
          />
          <h4 class="card-list__head">
            <span class="card-list__head--color">Второе мнениев онкологии</span>
            от экспертов мирового уровня
          </h4>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.services {
  margin-bottom: 20px;
  .sevices__header {
    margin-bottom: 44px;
    a {
      position: relative;
      font-size: clamp(13px, 3vw, 16px);
      font-weight: 700;
      line-height: 100%;
      letter-spacing: 0%;
      color: var(--second-head-link-color);
      text-decoration: none;
      &::after {
        position: absolute;
        left: 50%;
        bottom: -3px;
        height: 1px;
        content: "";
        width: 0;
        background-color: rgb(1, 74, 32);
        transition: width 0.5s ease, left 0.5s ease;
      }
      &:hover::after {
        width: 100%;
        left: 0;
      }
      &:hover {
        color: rgb(1, 74, 32);
      }
    }
  }
  .services__card-list {
    list-style-type: none;
    display: flex;
    @media (max-width: 768px) {
      flex-direction: column;
      align-items: flex-start;
    }
    .services__card-item {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: center;
      padding: clamp(20px, 2vw, 30px) clamp(16px, 2vw, 25px);
      background-color: var(--second-background-card-color);
      flex: 1;
      img {
        transition: transform 0.3s ease;
      }
      &:hover {
        img {
          transform: scale(1.15);
        }
      }
      @media (max-width: 768px) {
        width: 100%;
        flex-direction: row;
        align-items: normal;
      }
      .card-list__head {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-top: 20px;
        font-size: clamp(12px, 1vw, 14px);
        font-weight: 400;
        line-height: 24px;
        letter-spacing: 0;
        text-align: center;
        .card-list__head--color {
          display: block;
          color: rgba(0, 121, 52, 1);
        }
        @media (max-width: 768px) {
          padding-top: 0;
          padding-left: 10px;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: flex-start;
          text-align: left;
        }
      }
    }
    .services__card-item:nth-child(2n - 1) {
      background-color: var(--main-background-card-color);
    }
  }
}
</style>
