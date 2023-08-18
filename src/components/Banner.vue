<template>
	<div class="banner flex-center width-max">
		<section class="first-column">
			<h1>A Simple Bookmark Manager</h1>
			<p>
				A clean and simple interface to organize your favourite websites. Open a
				new browser tab and see your sites load instantly. Try it for free.
			</p>
			<section class="get-in-btn flex-center">
				<ButtonComponent text="Get in on Chrome" color="softBlue" />
				<ButtonComponent text="Get in on Firefox" color="grayishBlue" />
			</section>
		</section>
		<section class="second-column">
			<img src="/images/illustration-hero.svg" alt="illustration hero image" />
		</section>
	</div>
	<div class="background-blue-block"></div>
</template>
<script setup>
	import ButtonComponent from './UI/ButtonComponent.vue';
</script>
<style scoped>
	.banner {
		margin-top: 80px;
		gap: 4rem;
		position: relative;
	}

	.first-column,
	.second-column {
		flex: 0 1 50%;
	}

	.background-blue-block {
		position: absolute;
		z-index: -1;
		background-color: var(--softBlue);
		width: 715px;
		height: 325px;
		border-radius: 150px 0 0 150px;
		top: 350px;
		right: 0;
	}

	h1 {
		font-size: 52px;
		margin-bottom: 20px;
	}

	p {
		font-size: 20px;
		max-width: 600px;
		margin-bottom: 20px;
		color: var(--grayishBlue);
	}

	.get-in-btn {
		gap: 2rem;
	}

	@media (max-width: 1300px) {
		.background-blue-block {
			right: -20px;
			width: 515px;
		}
	}

	@media (max-width: 1200px) {
		.background-blue-block {
			top: 250px;
			right: -20px;
			width: 515px;
		}
	}

	@media (max-width: 992px) {
		.banner {
			flex-direction: column-reverse;
			gap: 1rem;
		}

		.first-column {
			text-align: center;
		}

		.first-column p {
			max-width: fit-content;
		}

		h1 {
			font-size: 36px;
		}

		.get-in-btn {
			justify-content: center;
		}

		.background-blue-block {
			display: none;
		}
	}
</style>
