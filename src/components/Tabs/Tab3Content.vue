<template>
	<div class="tab flex-center">
		<section class="first-column">
			<img
				src="/images/illustration-features-tab-3.svg"
				alt="illustration features tab 1 image"
				class="img-90"
			/>
			<div class="background-blue-block-right"></div>
		</section>
		<section class="second-column">
			<h2 class="title-tabs">Share your bookmarks</h2>
			<p class="text-tabs">
				Easily share your bookmarks and collections with others. Create a
				shareable link that you can send at the click of a button.
			</p>
			<ButtonComponent text="More Info" color="softBlue" />
		</section>
	</div>
</template>
<script setup>
	import './Tabs.css';
	import ButtonComponent from '../UI/ButtonComponent.vue';
</script>
