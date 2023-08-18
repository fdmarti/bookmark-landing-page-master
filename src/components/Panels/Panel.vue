<template>
	<div class="accordion-btn" @click="onClickShowPanel">
		<span>{{ title }}</span>
		<img
			src="/images/icon-arrow-close.svg"
			alt="icon arrow close accordion"
			v-if="showPanel"
		/>
		<img src="/images/icon-arrow.svg" alt="icon arrow open accordion" v-else />
	</div>
	<div class="panel" v-if="showPanel">
		<p>{{ text }}</p>
	</div>
</template>
<script setup>
	import './Panel.css';
	import { ref } from 'vue';
	const { title, text } = defineProps(['title', 'text']);

	const showPanel = ref(false);

	const onClickShowPanel = () => (showPanel.value = !showPanel.value);
</script>
