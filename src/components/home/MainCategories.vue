<script setup>
// import ref from 'vue'
// import { RouterLink, RouterView } from 'vue-router'
import beverageImg from '@/assets/images/beverages-thumb.png'

import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/navigation';

// import required modules
import { Navigation } from 'swiper/modules';
const modules = [Navigation]
const breakpoints = {
  320: {  // For mobile devices
    slidesPerView: 3,
    spaceBetween: 10
  },
  640: {  // For tablets
    slidesPerView: 4,
    spaceBetween: 20
  },
  1024: { // For desktops
    slidesPerView: 6,
    spaceBetween: 30
  }
}
</script>

<template>
    <swiper :navigation="true" :modules="modules" :breakpoints="breakpoints" class="mySwiper">
        <swiper-slide class="category">
            <div class="cate-img">
                <img :src="beverageImg" alt="Beverages" class="container-fluid">
            </div>
            <h3>Beverages</h3>
        </swiper-slide>
        <swiper-slide class="category">
            <div class="cate-img">
                <img :src="beverageImg" alt="Beverages" class="container-fluid">
            </div>
            <h3>Beverages</h3>
        </swiper-slide>
        <swiper-slide class="category">
            <div class="cate-img">
                <img :src="beverageImg" alt="Beverages" class="container-fluid">
            </div>
            <h3>Beverages</h3>
        </swiper-slide>
  </swiper>
</template>

<style scoped>
.category{
    background: rgb(247 247 252/var(--tw-bg-opacity,1));
    border-radius: 1rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 200px;
    overflow-x: auto;
}

.category h3{
    font-size: 12px;
}
.category .cate-img{
    width: 100%;
}
</style>