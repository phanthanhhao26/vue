<script setup>
import Hero from './sections/Hero.vue';
import Nav from './components/Nav.vue';
import PopularProducts from './sections/PopularProducts.vue';
import SuperQuality from './sections/SuperQuality.vue';
import Services from './sections/Services.vue';
import SpecialOffer from './sections/SpecialOffer.vue';
import CustomerReviews from './sections/CustomerReviews.vue';
</script>

<template>
	<main class="relative">
		<Nav></Nav>
		<section class="xl:padding-l wide:padding-r padding-b">
			<Hero />
		</section>
		<section class="padding">
			<PopularProducts />
		</section>
		<section class="padding">
			<SuperQuality />
		</section>
		<section class="padding-x py-10">
			<Services />
		</section>
		<section class="padding">
			<SpecialOffer />
		</section>
		<section class="bg-pale-blue padding">
			<CustomerReviews />
		</section>
	</main>
</template>
