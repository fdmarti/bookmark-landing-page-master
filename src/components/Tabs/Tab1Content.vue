<template>
	<div class="tab flex-center">
		<section class="first-column">
			<img
				src="/images/illustration-features-tab-1.svg"
				alt="illustration features tab 1 image"
			/>
			<div class="background-blue-block-right"></div>
		</section>
		<section class="second-column">
			<h2 class="title-tabs">Bookmark in one click</h2>
			<p class="text-tabs">
				Organize your bookmarks however you like. Our simple drag-and-drop
				interface gives you complete control over how you manage your favourite
				sites.
			</p>
			<ButtonComponent text="More Info" color="softBlue" />
		</section>
	</div>
</template>
<script setup>
	import './Tabs.css'
	import ButtonComponent from '../UI/ButtonComponent.vue';
</script>
