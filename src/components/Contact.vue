<template>
	<div class="contact-us">
		<p>5,000 + already joined</p>
		<h3>Stay up-to-date with what we’re doing</h3>
		<FormComponent />
	</div>
</template>
<script setup>
	import FormComponent from './Form/FormComponent.vue';
</script>
<style scoped>
	.contact-us {
		background-color: var(--softBlue);
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1rem;
		padding: 30px 20px 80px 20px;
	}

	p {
		font-size: 13px;
		letter-spacing: 5px;
		color: var(--white);
		text-transform: uppercase;
		padding: 30px 0 20px 0;
	}

	h3 {
		font-size: 32px;
		color: var(--white);
		font-weight: 500;
		max-width: 450px;
		text-align: center;
	}
</style>
