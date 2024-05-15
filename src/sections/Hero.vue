<script setup>
import Button from '../components/Button.vue'
import bigShoe1 from '../assets/images/big-shoe1.png'
import thumbnailShoe1 from '../assets/images/thumbnail-shoe1.svg'
import thumbnailShoe2 from '../assets/images/thumbnail-shoe2.svg'
import thumbnailShoe3 from '../assets/images/thumbnail-shoe3.svg'
import { shoes, statistics } from '../constants/index'
import ShoeCard from '../components/ShoeCard.vue'
</script>

<template>
    <section
        id="home"
        class="w-full flex xl:flex-row flex-col justify-center min-h-screen gap-10 max-container"    
    >
        <div class="relative xl:w-2/5 flex flex-col justify-center items-start w-full max-xl:padding-x pt-28">
            <p class="text-xl font-montserrat text-coral-red">Our Summer Collections</p>
            <h1 class="mt-10 font-palanquin text-8xl max-sm:text-[72px] max-sm:leading-[82px] font-bold">
                <span class="xl:bg-white xl:whitespace-nowrap relative z-10 pr-10">The New Arrival</span>
                <br />
                <span class="text-coral-red inline-block mt-3">Nike</span>
                Shoes
            </h1>
            <p class="font-montserrat text-gray-500 text-xl leading-8 mt-6 mb-14 sm:max-w-sm">Discover stylish Nike arrivals, quality comfort, and innovation for your active life.</p>
            <Button label="Shop now" @click="testOnClick" />
            <div class="flex justify-start items-start flex-wrap w-full mt-20 gap-16">
                <div v-for="statistic in statistics">
                    <p class="text-4xl font-palanquin font-bold">{{ statistic.value }}</p>
                    <p class="leading-7 font-montserrat text-gray-500">{{ statistic.label }}</p>
                </div>
            </div>
        </div>
        
        <div class="relative flex-1 flex justify-center items-center
            xl:min-h-screen max-xl:py-40 bg-primary bg-hero bg-cover bg-center">
            <img
                :src="bigShoe1"
                alt="shoe collection"
                width="610"
                height="500"
                class="object-contain relative z-10"
            >
            <div class="flex sm:gap-6 gap-4 absolute -bottom-[5%]
                sm:left-[10%] max-sm:px-6">
                <ShoeCard
                    v-for="shoe in shoes"
                    :item="shoe"
                />
                <!-- <div>
                    <div class="border-2 rounded-xl border-red-400 border-transparent
                        cursor-pointer max-sm:flex-1">
                        <div class="flex justify-center items-center bg-card bg-center
                            bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4">
                            <img
                                :src="thumbnailShoe1"
                                alt="shoe collection"
                                width="127"
                                height="103"
                            >
                        </div>
                    </div>
                </div>
                <div>
                    <div class="border-2 rounded-xl border-red-400 border-transparent
                        cursor-pointer max-sm:flex-1">
                        <div class="flex justify-center items-center bg-card bg-center
                            bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4">
                            <img
                                :src="thumbnailShoe2"
                                alt="shoe collection"
                                width="127"
                                height="103"
                            >
                        </div>
                    </div>
                </div>
                <div>
                    <div class="border-2 rounded-xl border-red-400 border-transparent
                        cursor-pointer max-sm:flex-1">
                        <div class="flex justify-center items-center bg-card bg-center
                            bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4">
                            <img
                                :src="thumbnailShoe3"
                                alt="shoe collection"
                                width="127"
                                height="103"
                            >
                        </div>
                    </div>
                </div> -->
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        methods: {
            testOnClick() {
                alert('Button clicked!!!')
            }
        }
    }
</script>