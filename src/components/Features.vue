<template>
	<section class="features width-max">
		<h2>Features</h2>
		<p>
			Our aim is to make it quick and easy for you to access your favourite
			websites. Your bookmarks sync between your devices so you can access them
			on the go.
		</p>
		<TabComponent />
	</section>
</template>
<script setup>
	import TabComponent from './UI/TabComponent.vue';
</script>
<style scoped>
	.features {
		margin-top: 100px;
		text-align: center;
		padding: 0 20px;
	}

	h2 {
		font-size: 36px;
		margin-bottom: 20px;
	}

	p {
		width: 500px;
		margin: 0 auto;
		color: var(--grayishBlue);
		font-size: 18px;
	}

	@media (max-width: 992px) {
		h2 {
			font-size: 36px;
		}

		p {
			width: auto;
		}
	}
</style>
