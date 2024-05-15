<script setup>
import customer1 from "../assets/images/customer1.jpeg"
import customer2 from "../assets/images/customer2.svg"
import ReviewCard from "../components/ReviewCard.vue";
import { reviews } from "../constants/index.js"
</script>

<template>
    <section class="max-container">
        <h3 class="font-palanquin text-center text-4xl font-bold">
            What Our
            <span class="text-coral-red"> Customers </span>
            Say?
        </h3>
        <p class="info-text m-auto mt-4 max-w-lg text-center">Hear genuine stories from our satisfied customers about their exceptional experiences with us.</p>

        <div class="mt-24 flex flex-1 justify-evenly items-center max-lg:flex-col gap-14">
            <ReviewCard
                v-for="review in reviews"
                :key="review.customerName"
                :imgURL="review.imgURL"
                :customerName="review.customerName"
                :rating="review.rating"
                :feedback="review.feedback"
            />
        </div>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                reviews: reviews
            }
        }
    }
</script>