<script setup>
import SwiperSlider from "./components/Swiper-slider.vue";
import VButton from "./components/VButton.vue";

</script>

<template>
  <div class="main">
    <div class="main-container">
      <!-- Title -->
      <div class="title">
        <div class="title-color">ОСТАВЬТЕ ЗАЯВКУ</div>
        И ВАМ ПЕРЕЗВОНИТ <br> МЕНЕДЖЕР, КОТОРЫЙ
      </div>
      <!-- List -->
      <div class="list">
        <ul>
          <li>
            <span
              ><b>Объяснит,</b> чем может отличаться дешевое окно от других
              предложений на рынке</span
            >
          </li>
          <li>
            <span><b>Ответит</b> на все волнующие Вас вопросы</span>
          </li>
          <li>
            <span><b>Согласует</b> время бесплатного выезда замерщика</span>
          </li>
        </ul>
      </div>
      <VButton/>
    </div>
    <SwiperSlider />
  </div>
</template>
