<template>
	<div class="extension width-max">
		<h2>Download the extension</h2>
		<p class="sub-title">
			We’ve got more browsers in the pipeline. Please do let us know if you’ve
			got a favourite you’d like us to prioritize.
		</p>
		<section class="cards-browsers flex-center">
			<CardComponent
				title="Add to Chrome"
				url-image="logo-chrome.svg"
				text="Minimum version 62"
				top="0"
			/>
			<CardComponent
				title="Add to Firefox"
				url-image="logo-firefox.svg"
				text="Minimum version 55"
				top="40px"
			/>
			<CardComponent
				title="Add to Opera"
				url-image="logo-opera.svg"
				text="Minimum version 46"
				top="80px"
			/>
		</section>
	</div>
</template>
<script setup>
	import { CardComponent } from './UI';
</script>

<style scoped>
	.extension {
		padding: 30px 20px 150px 20px;
		text-align: center;
	}

	h2 {
		font-size: 46px;
		margin-bottom: 10px;
	}

	.sub-title {
		font-size: 20px;
		max-width: 600px;
		margin: 0 auto 60px auto;
		color: var(--grayishBlue);
	}

	.cards-browsers {
		justify-content: center;
		position: relative;
		gap: 6rem;
	}

	@media (max-width: 992px) {
		h2 {
			font-size: 36px;
		}

		.sub-title {
			width: auto;
		}

		.cards-browsers {
			gap: 0;
			flex-direction: column;
		}
	}
</style>
