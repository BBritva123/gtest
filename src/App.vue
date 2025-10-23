<template>
  <section>
    <div class="container">
      <h2 class="header">Медицинские услуги</h2>
      <HeroSwiper></HeroSwiper>
    </div>
    <SecondServices></SecondServices>
    <MainServices></MainServices>
  </section>
</template>

<script setup lang="ts">
import HeroSwiper from "@/components/HeroSwiper.vue";
import SecondServices from "@/components/SecondServices.vue";
import MainServices from "@/components/MainServices.vue";
</script>
