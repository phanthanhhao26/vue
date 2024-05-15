<script setup>
import offer from '../assets/images/offer.svg'
import Button from '../components/Button.vue'
</script>

<template>
    <section class="flex justify-wrap items-center max-xl:flex-col-reverse gap-10 max-container">
        <div class="flex-1">
            <img
                :src="offer"
                width="773"
                height="687"
                class="object-contain w-full"
            />
        </div>
        <div>
            <h2 class="font-palanquin text-4xl capitalize font-bold
                lg:max-w-lg">
                <span class="text-coral-red"> Special</span> Offer
            </h2>
            <p class="mt-4 lg:max-w-lg info-text">
                Embark on a shopping journey that redefines your experience with
				unbeatable deals. From premier selections to incredible savings, we
				offer unparalleled value that sets us apart.
            </p>
            <p class="mt-6 lg:max-w-lg info-text">
                Navigate a realm of possibilities designed to fulfill your unique
				desires, surpassing the loftiest expectations. Your journey with us is
				nothing short of exceptional.
            </p>
            <div class="flex mt-11 flex-wrap gap-4">
                <Button label="Shop now" />
                <Button label="Learn more" />
            </div>
        </div>
    </section>
</template>