<script setup>
import headerLogo from '../assets/images/header-logo.svg';
import hamburger from '../assets/icons/hamburger.svg';
import bigShoe1 from '../assets/images/big-shoe1.png';
</script>

<template>
    <header class="padding-x py-8 absolute z-10 w-full">
        <nav class="flex justify-between items-center max-container">
            <a href="/">
                <img
                    :src="headerLogo"
                    alt="Logo"
                    width="130"
                    height="29"
                />
            </a>
			<ul class="flex-1 flex justify-center items-center gap-16 max-lg:hidden">
				<li>
					<a
						href=""
						class="font-montserrat leading-normal text-lg text-slate-gray"
					>
						Home
					</a>
				</li>
				<li>
					<a
						href=""
						class="font-montserrat leading-normal text-lg text-slate-gray"
					>
						About Us
					</a>
				</li>
				<li>
					<a
						href=""
						class="font-montserrat leading-normal text-lg text-slate-gray"
					>
						Products
					</a>
				</li>
				<li>
					<a
						href=""
						class="font-montserrat leading-normal text-lg text-slate-gray"
					>
						Contact Us
					</a>
				</li>
			</ul>
			<div class="hidden max-lg:block">
				<img
					:src="hamburger"
					alt="Hamburger"
					width="25"
					height="25"
				/>
			</div>
        </nav>
    </header>
</template>