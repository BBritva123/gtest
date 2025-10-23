<template>
  <aside class="our-services">
    <div class="container">
      <h3 class="head our-services__head">ДРУГИЕ МЕДИЦИНСКИЕ УСЛУГИ</h3>
      <ul class="our-services__list">
        <li class="our-services__item">
          <a href="#" class="our-services__link"> УЗИ </a>
        </li>
        <li class="our-services__item">
          <a href="#" class="our-services__link">
            УЗИ дома <span>– бесплатный выезд</span>
          </a>
        </li>
        <li class="our-services__item">
          <a href="#" class="our-services__link"> ЭКГ </a>
        </li>
        <li class="our-services__item">
          <a href="#" class="our-services__link">
            ЭКГ дома <span>– бесплатный выезд</span>
          </a>
        </li>
        <li class="our-services__item">
          <a href="#" class="our-services__link"> Лечение Сургитрон </a>
        </li>
        <li class="our-services__item">
          <a href="#" class="our-services__link"> Кольпоскопия </a>
        </li>
      </ul>
    </div>
  </aside>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.our-services {
  margin-bottom: 14px;
  .our-services__head {
    margin-bottom: 16px;
    color: var(--second-head-color);
    font-size: clamp(10px, 1vw, 11px);
    font-weight: 700;
    line-height: 100%;
    letter-spacing: 0.4px;
    text-align: left;
    @media (max-width: 576px) {
      margin-bottom: 20px;
      letter-spacing: -0.1px;
    }
  }
  .our-services__list {
    display: flex;
    max-width: 80%;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: flex-start;
    align-items: center;
    font-size: clamp(13px, 3vw, 16px);
    font-weight: 300;
    line-height: clamp(28px, 3vw, 32px);
    letter-spacing: 0;
    text-align: left;
    overflow: hidden;
    @media (max-width: 768px) {
      flex-direction: column;
      align-items: flex-start;
      max-width: 100%;
    }
    .our-services__item {
      margin-right: 33px;
      list-style-type: disc;
      .our-services__link {
        position: relative;
        color: var(--main-text-color);
        text-decoration: none;
        transition: color 0.3s ease;
        span {
          color: var(--second-swiper-color);
        }
        &::after {
          position: absolute;
          left: 50%;
          bottom: -3px;
          height: 1px;
          content: "";
          width: 0;
          background-color: var(--second-swiper-color);
          transition: width 0.5s ease, left 0.5s ease;
        }
        &:hover::after {
          width: 100%;
          left: 0;
        }
        &:hover {
          color: var(--second-swiper-color);
        }
      }
    }
    .our-services__item::marker {
      color: var(--marker-color);
      font-size: 15px;
    }
    .our-services__item:first-child {
      list-style-type: none;
    }
    .our-services__item:not(:first-child) {
      padding-left: 2px;
    }
  }
}
</style>
