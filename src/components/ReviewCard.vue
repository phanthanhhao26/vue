<script setup>
import star from "../assets/icons/star.svg"

defineProps({
    imgURL: {
        type: String,
        required: true
    },
    customerName: {
        type: String,
        required: true
    },
    rating: {
        type: Number,
        required: true
    },
    feedback: {
        type: String,
        required: true
    }
})
</script>

<template>
    <div class="flex flex-col justify-center items-center">
        <img
            :src="imgURL"
            alt="customer"
            class="rounded-full object-cover w-[120px] h-[120px]"
        />
        <p class="mt-6 max-w-sm text-center info-text">{{ feedback }}</p>
        <div class="mt-3 flex justify-center items-center gap-2.5">
            <img
                :src="star"
                width="24"
                height="24"
                class="object-contain m-0"
            />
            <p class="text-xl font-montserrat text-slate-gray">({{ rating }})</p>
        </div>
        <h3 class="mt-2 font-palanquin text-3xl text-center font-bold">{{ customerName }}</h3>
    </div>
</template>