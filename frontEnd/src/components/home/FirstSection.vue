<template>
    <div class="style-00">
        <div class="style-01">
            <h1>Modern Minimalist Furniture</h1>
            <p>Discover a curated collection of handcrafted pieces designed to transform your living spaces into
                expressions of your unique taste and lifestyle.</p>
            <button type="button">Explore More</button>
        </div>
        <div class="style-02">
            <div class="style-03">
                <SwiperPagination class="style-05" :images="images" />
            </div>
            <div class="style-04">
            </div>
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
.style-00 {
    @apply grid grid-rows-2 p-4 gap-4
}

.style-01 {
    @apply row-span-1 px-60 flex flex-col justify-center items-end rounded-lg gap-2 max-h-96;
    @apply bg-cyan-600;
}

.style-02 {
    @apply grid grid-cols-3 row-span-1 gap-4 
}

.style-03 {
    @apply col-span-2 max-h-96 rounded-lg
}

.style-04 {
    @apply col-span-1 bg-cover bg-center rounded-lg;
    background-image: url(/images/image-01.jpg)
}

.style-05 {
    @apply rounded-lg
}

h1 {
    @apply text-6xl font-bold w-full text-center;
    @apply text-white;
}

p {
    @apply text-sm font-light w-1/2;
    @apply text-white;
}

button {
    @apply border-2 px-4 py-2 rounded-full font-semibold shadow-lg;
    @apply bg-green-600 border-green-600 text-gray-200 hover:border-gray-800;
}
</style>