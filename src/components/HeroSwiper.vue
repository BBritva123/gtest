<template>
  <div class="swiper__container">
    <swiper
      class="hero__swiper"
      :slides-per-view="1"
      :space-between="5"
      :breakpoints="{
        320: { slidesPerView: 1, spaceBetween: 5 },
        576: { slidesPerView: 2, spaceBetween: 8 },
        968: { slidesPerView: 3, spaceBetween: 12 },
      }"
      loop
      auto-height
    >
      <swiper-slide>
        <img
          src="/img/swiper/sw1-v.webp"
          alt="Анализы дома"
          class="swiper__img"
          loading="lazy"
        />
        <div class="swiper__content">
          <h3 class="swiper__head">Анализы дома</h3>
          <p class="swiper__description">
            Бесплатный выезд. Для детей и взрослых. Удобно и быстро.
          </p>
        </div>
        <button
          class="swiper__button"
          aria-label="Получить бесплатную консультацию"
        >
          Бесплатно
        </button>
      </swiper-slide>
      <swiper-slide>
        <img
          src="/img/swiper/sw2-v.webp"
          alt="МРТ"
          class="swiper__img"
          loading="lazy"
        />
        <div class="swiper__content">
          <h3 class="swiper__head">МРТ</h3>
          <p class="swiper__description">
            Запись на магнитно-резонансную томографию. 8 видов скрининга.
          </p>
        </div>
        <button class="swiper__button" aria-label="Запись от 1690 рублей">
          От 1 690 Р
        </button>
      </swiper-slide>
      <swiper-slide>
        <img
          src="/img/swiper/sw3-v.webp"
          alt="Срочные анализы CITO"
          class="swiper__img"
          loading="lazy"
        />

        <div class="swiper__content">
          <h3 class="swiper__head">Срочные анализы CITO</h3>
          <p class="swiper__description">
            Быстрая диагностика в день обращения. Более 30 видов анализов.
          </p>
        </div>
        <button
          class="swiper__button"
          aria-label="Результаты будут готовы в 14.00 часов"
        >
          Результаты в 14:00
        </button>
      </swiper-slide>
      <swiper-slide>
        <img
          src="/img/swiper/sw2-v.webp"
          alt="Тест"
          class="swiper__img"
          loading="lazy"
        />
        <div class="swiper__content">
          <h3 class="swiper__head">Срочные анализы CITO</h3>
          <p class="swiper__description">
            Быстрая диагностика в день обращения. Более 30 видов анализов.
          </p>
        </div>
        <button
          class="swiper__button"
          aria-label="Кнопка для теста количества слайдов"
        >
          Тест слайдов
        </button>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup lang="ts">
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
</script>

<style scoped lang="scss">
.swiper {
  margin-bottom: clamp(34px, 5%, 49px);
  :deep(.swiper-wrapper) {
    align-items: stretch;
  }
  :deep(.swiper-slide) {
    position: relative;
    padding: 32px 40px 101px 40px;
    border-radius: 4px;
    min-height: 280px;
    &:hover {
      .swiper__img {
        transform: scale(1.01);
      }
    }
    .swiper__img {
      position: absolute;
      left: 0;
      top: 0;
      right: 0;
      bottom: 0;
      width: 100%;
      height: 100%;
      transition: transform 0.3s ease;
    }
    .swiper__content {
      position: relative;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 100%;
      z-index: 200;
      color: white;
      flex: 1;
      .swiper__head {
        max-width: 90%;
        font-size: clamp(15px, 3vw, 24px);
        font-weight: 600;
        line-height: clamp(20px, 3vw, 28px);
        letter-spacing: 0.5px;
      }
      .swiper__description {
        font-size: 16px;
        font-weight: 400;
        line-height: 22px;
        letter-spacing: 0;
      }
    }
    .swiper__button {
      position: absolute;
      bottom: 41px;
      display: flex;
      flex-direction: row;
      align-items: center;
      padding: 8px 18px;
      color: var(--swiper-text-color);
      background-color: var(--second-swiper-color);
      border: none;
      outline: 1px solid transparent;
      border-radius: 20px;
      cursor: pointer;
      transition: outline 0.3s ease, color 0.3s ease, background-color 0.3s ease;
      &:hover {
        color: #ebe3e3;
        background-color: rgb(202, 55, 2);
        outline: 1px solid rgb(202, 55, 2);
      }
    }
  }
}
</style>
