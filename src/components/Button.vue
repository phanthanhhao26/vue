<script setup>
import arrowRight from "../assets/icons/arrow-right.svg"

defineProps({
    label: {
        type: String,
        required: true,
    }
})
</script>

<template>
    <button class="flex justify-center items-center gap-2
        px-7 py-4 border font-montserrat text-lg leading-none
        bg-red-400 text-white border-red-400 rounded-full w-full">
        {{ label }}
        <img
            :src="arrowRight"
            alt="arrow right icon"
            class="ml-2 rounded-full w-5 h-5"
        />
    </button>
</template>