<template>
	<section class="panels">
		<Panel
			title="What is Bookmark?"
			text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt
				justo eget ultricies fringilla. Phasellus blandit ipsum quis quam ornare
				mattis."
		/>

		<Panel
			title="How can I request a new browser?"
			text="Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa,
				ultricies non ligula. Suspendisse imperdiet. Vivamus luctus eros aliquet
				convallis ultricies. Mauris augue massa, ultricies non ligula.
				Suspendisse imperdie tVivamus luctus eros aliquet convallis ultricies.
				Mauris augue massa, ultricies non ligula. Suspendisse imperdiet."
		/>

		<Panel
			title="Is there a mobile app?"
			text="Sed consectetur quam id neque fermentum accumsan. Praesent luctus
				vestibulum dolor, ut condimentum urna vulputate eget. Cras in ligula
				quis est pharetra mattis sit amet pharetra purus. Sed sollicitudin ex et
				ultricies bibendum."
		/>

		<Panel
			title="What about other Chromium browsers?"
			text="Integer condimentum ipsum id imperdiet finibus. Vivamus in placerat mi,
				at euismod dui. Aliquam vitae neque eget nisl gravida pellentesque non
				ut velit."
		/>
	</section>
</template>
<script setup>
	import Panel from '../Panels/Panel.vue';
</script>
<style scoped>
	.panels {
		max-width: 600px;
		display: flex;
		flex-direction: column;
		margin: 0 auto 50px auto;
	}
</style>
