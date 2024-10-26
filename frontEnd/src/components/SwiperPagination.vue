<template>
    <swiper :pagination="true" :autoplay="{ delay: 3000 }" :modules="[Pagination, Autoplay]" class="mySwiper">
        <swiper-slide v-for="(image, index) in images" :key="index">
            <img :src="image" :alt="`Slide ${index + 1}`" />
        </swiper-slide>
    </swiper>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination, Autoplay  } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/autoplay'

defineProps({
    images: {
        type: Array,
        required: true,
    },
});
</script>

<style scoped>
.swiper {
    width: 100%;
    height: 100%;
}

.swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
}

.swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>