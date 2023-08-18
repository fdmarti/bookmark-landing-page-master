<template>
	<div class="tab flex-center">
		<section class="first-column">
			<img
				src="/images/illustration-features-tab-2.svg"
				alt="illustration features tab 2 image"
				class="img-90"
			/>
			<div class="background-blue-block-right"></div>
		</section>
		<section class="second-column">
			<h2 class="title-tabs">Intelligent search</h2>
			<p  class="text-tabs">
				Our powerful search feature will help you find saved sites in no time at
				all. No need to trawl through all of your bookmarks.
			</p>
			<ButtonComponent text="More Info" color="softBlue" />
		</section>
	</div>
</template>
<script setup>
	import './Tabs.css'
	import ButtonComponent from '../UI/ButtonComponent.vue';
</script>
