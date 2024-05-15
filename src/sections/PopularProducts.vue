<script setup>
import shoe4 from '../assets/images/shoe4.svg'
import shoe5 from '../assets/images/shoe5.svg'
import shoe6 from '../assets/images/shoe6.svg'
import shoe7 from '../assets/images/shoe7.svg'
import star from '../assets/icons/star.svg'
import { products } from '../constants/index.js'
import PopularProductCard from '../components/PopularProductCard.vue'
</script>


<template>
    <section id="products" class="max-container max-sm:mt-12">
        <div class="flex flex-col justify-start1 gap-5">
            <h2 class="text-4xl font-palanquin font-bold">Our
            <span class="text-coral-red"> Popular</span> Products</h2>
            <p class="lg:max-w-lg mt-2 font-montserrat text-slate-gray">Experience top-notch quality and style with our sought-after
                selections. Discover a world of comfort, design, and value</p>
        </div>
        <div class="mt-16 grid
            lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 grid-cols-1
            sm:gap-4 gap-14">
            <PopularProductCard
                v-for="product in products"
                :key="product.name"
                :name="product.name"
                :imgURL="product.imgURL"
                :price="product.price"
            />
        </div>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                products
            }
        }
    }
</script>