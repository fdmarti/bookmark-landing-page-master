<template>
	<div class="card" :style="{ top: top }">
		<img :src="`/images/${urlImage}`" :alt="`${title} logo`" />
		<h3>{{ title }}</h3>
		<p>{{ text }}</p>
		<div class="dotted-divider"></div>
		<ButtonComponent
			class="btn-card"
			text="Add & Install Extension"
			color="softBlue"
		/>
	</div>
</template>
<script setup>
	import ButtonComponent from './ButtonComponent.vue';
	const { title, urlImage, text, top } = defineProps([
		'title',
		'urlImage',
		'text',
		'top',
	]);
</script>
<style scoped>
	.card {
		padding: 20px;
		border-radius: 10px;
		box-shadow: 0px 2px 20px -5px var(--grayishBlue);
		height: 300px;
		position: relative;
	}

	img {
		width: 100px;
		margin-bottom: 30px;
	}

	h3 {
		margin-bottom: 10px;
	}

	p {
		font-size: 18px;
		margin-bottom: 20px;
		color: var(--grayishBlue);
	}

	.dotted-divider {
		width: 100%;
		height: 10px;
		background: url('/images/bg-dots.svg') no-repeat center/contain;
	}

	.btn-card {
		margin: 30px 0;
	}
</style>
