<template>
    <div class="style-00">
        <div class="style-03">
            <button v-for="(step, index) in stepNames" :key="step.name" @click="goToStep(index + 1)"
                :class="{ active: currentStep === index + 1 }" class="card">
                <div class="style-01">
                    <img :src="step.image" alt="" class="style-02" />
                    {{ step.name }}
                </div>
            </button>
        </div>
        <div>
            <div v-if="currentStep === 1">
                <div>
                    <h1>Daily offer</h1>
                    <p>
                        check out our daily offers that can combine big discounts on some products. Offers may change
                        every, do not miss your chance.
                    </p>
                    <button>open store</button>
                </div>
                <div>
                    <img src="../../../public/images/secondSection/image-chair-2.jpg" alt="" class="" />
                </div>
                <div>
                    <img src="../../../public/images/secondSection/image-chair-3.jpg" alt="" class="" />
                </div>
            </div>
            <div v-else-if="currentStep === 2">Conteúdo da Janela 2</div>
            <div v-else-if="currentStep === 3">Conteúdo da Janela 3</div>
            <div v-else-if="currentStep === 4">Conteúdo da Janela 4</div>
            <div v-else-if="currentStep === 5">Conteúdo da Janela 5</div>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const stepNames = [
    { name: 'chairs', image: 'images/secondSection/image-chair.png' },
    { name: 'sofa', image: 'images/secondSection/image-sofa.png' },
    { name: 'cabinet', image: 'images/secondSection/image-cabinet.png' },
    { name: 'wardrobe', image: 'images/secondSection/image-wardrobe.png' },
    { name: 'armchair', image: 'images/secondSection/image-armchair.png' },
]



const currentStep = ref(1)
let interval = null

const goToStep = (step) => {
    currentStep.value = step
}

const nextStep = () => {
    currentStep.value = currentStep.value < 5 ? currentStep.value + 1 : 1
}

const startAutoNextStep = () => {
    interval = setInterval(nextStep, 10000)
}

const stopAutoNextStep = () => {
    clearInterval(interval)
}

onMounted(startAutoNextStep)
onBeforeUnmount(stopAutoNextStep)
</script>

<style scoped>
.style-00 {
    @apply py-4 px-14
}

.style-02 {
    @apply size-32
}

.style-01 {
    @apply flex flex-col gap-4
}

.style-03 {
    @apply grid grid-cols-5 gap-4
}

button.active {
    @apply bg-emerald-200 border-gray-800
}

.card {
    @apply p-4 text-xl border-2 capitalize font-bold rounded-lg flex justify-center items-center shadow-lg;
    @apply bg-slate-200 border-slate-200 text-gray-900;
}
</style>
