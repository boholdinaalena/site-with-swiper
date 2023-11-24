<template>
  <div class="slider-container">
    <h1>Работают для вас:</h1>
    <swiper
      :modules="modules"
      :slidesPerView="3"
      navigation
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide v-for="employee in employees">
        <div>
          <div class="box-year">
            с {{ employee.year }} <br />
            года
          </div>
          <div class="box-information">
            <div class="employee-name">{{ employee.name }}</div>
            <div>
              <div class="employee-calls">{{ employee.calls }}</div>
              <div class="box-text-calls">звонков принято</div>
            </div>
          </div>
          <img
            class="img-slide"
            :src="`src/assets/${employee.photo}`"
            :alt="photo"
          />
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
// import Swiper core and required modules
import { Navigation, Pagination, Scrollbar, A11y } from "swiper/modules";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

// Import Swiper styles
export default {
  components: {
    Swiper,
    SwiperSlide,
  },

  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation, Pagination, Scrollbar, A11y],
      employees: [
        {
          name: "Екатерина Игнатова",
          photo: "Екатерина Игнатова.png",
          year: "2009",
          calls: "27 921",
        },
        {
          name: "Эльвира Эксанова",
          photo: "Эльвира Эксанова.png",
          year: "2015",
          calls: "8 515",
        },
        {
          name: "Михаил Демин",
          photo: "Михаил Демин.png",
          year: "2005",
          calls: "10 423",
        },
        {
          name: "Михаил Демин",
          photo: "Михаил Демин.png",
          year: "2005",
          calls: "10 423",
        },
        {
          name: "Михаил Демин",
          photo: "Михаил Демин.png",
          year: "2005",
          calls: "10 423",
        },
      ],
    };
  },
};
</script>
