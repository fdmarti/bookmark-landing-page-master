<template>
	<div class="faq width-max">
		<h3>Frequently Asked Questions</h3>
		<p>
			Here are some of our FAQs. If you have any other questions you’d like
			answered please feel free to email us.
		</p>

		<AccordionComponent />
		<ButtonComponent text="More Info" color="softBlue" />
	</div>
</template>
<script setup>
	import { ButtonComponent, AccordionComponent } from './UI';
</script>
<style scoped>
	.faq {
		padding: 30px 20px 150px 20px;
		text-align: center;
		max-width: 670px;
		margin: 0 auto;
	}

	h3 {
		font-size: 46px;
		margin-bottom: 10px;
	}

	p {
		font-size: 20px;
		max-width: 600px;
		margin: 0 auto 60px auto;
		color: var(--grayishBlue);
	}

	@media (max-width: 992px) {
		.faq {
			padding: 30px 20px;
		}
	}
</style>
