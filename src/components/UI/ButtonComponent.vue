<template>
	<button class="btn" :class="[color, { upper: upper }]">{{ text }}</button>
</template>
<script setup>
	const { text, color, upper } = defineProps(['text', 'color', 'upper']);
</script>
<style scoped>
	.btn {
		border-radius: 5px;
		padding: 10px 35px;
		border: 2px solid transparent;
		font-size: 14px;
		box-shadow: 0px 4px 12px -1px #00000052;
		font-weight: 500;
	}

	.btn:hover {
		cursor: pointer;
	}

	.upper {
		text-transform: uppercase;
	}

	.softBlue {
		background-color: var(--softBlue);
		color: var(--white);
	}

	.softRed {
		background-color: var(--softRed);
		color: var(--white);
	}

	.softRed:hover {
		color: var(--softRed);
		background-color: var(--white);
		border: 2px solid var(--softRed) !important;
	}

	.softBlue:hover {
		color: var(--softBlue);
		background-color: var(--white);
		border: 2px solid var(--softBlue) !important;
	}

	.grayishBlue:hover {
		color: var(--grayishBlue);
		background-color: var(--white);
		border: 2px solid var(--grayishBlue) !important;
	}
</style>
