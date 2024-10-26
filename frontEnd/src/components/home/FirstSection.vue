<template>
    <div class="section-container">
        <div class="text-content">
            <h1>Modern Minimalist Furniture</h1>
            <p>Discover a curated collection of handcrafted pieces designed to transform your living spaces into
                expressions of your unique taste and lifestyle.</p>
            <button type="button">Explore More</button>
        </div>
        <div class="image-content">
            <div class="swiper-container">
                <SwiperPagination class="pagination" :images="images" />
            </div>
            <div class="highlighted-image"></div>
        </div>
    </div>
</template>

<script setup>
import SwiperPagination from '../../components/SwiperPagination.vue'

const images = [
    'images/image-slide-1.jpg',
    'images/image-slide-1.jpg',
    'images/image-slide-1.jpg',
];
</script>

<style scoped>
.section-container {
    @apply grid grid-rows-2 p-4 gap-4;
}

.text-content {
    @apply row-span-1 px-60 flex flex-col justify-center items-end rounded-lg gap-2 max-h-96 bg-cyan-600;
}

.image-content {
    @apply grid grid-cols-3 row-span-1 gap-4;
}

.swiper-container {
    @apply col-span-2 max-h-96 rounded-lg;
}

.highlighted-image {
    @apply col-span-1 bg-cover bg-center rounded-lg;
    background-image: url(/images/image-01.jpg);
}

.pagination {
    @apply rounded-lg;
}

h1 {
    @apply text-6xl font-bold w-full text-center text-white;
}

p {
    @apply text-sm font-light w-1/2 text-white;
}

button {
    @apply border-2 px-4 py-2 rounded-full font-semibold shadow-lg;
    @apply bg-green-600 border-green-600 text-gray-200 hover:border-gray-800;
}
</style>
