<template>
	<div class="tab">
		<section class="tab-options flex-center">
			<button
				class="btn-tab"
				:class="{ active: tabsState[0] }"
				@click="onChangeTabsState(0)"
			>
				Simple Bookmarking
			</button>
			<button
				class="btn-tab"
				:class="{ active: tabsState[1] }"
				@click="onChangeTabsState(1)"
			>
				Speedy Searching
			</button>
			<button
				class="btn-tab"
				:class="{ active: tabsState[2] }"
				@click="onChangeTabsState(2)"
			>
				Easy Sharing
			</button>
		</section>
		<section class="tab-content">
			<Tab1Content v-if="tabsState[0]" />
			<Tab2Content v-if="tabsState[1]" />
			<Tab3Content v-if="tabsState[2]" />
		</section>
	</div>
</template>
<script setup>
	import { ref } from 'vue';
	import { Tab1Content, Tab2Content, Tab3Content } from '../Tabs';

	const tabsState = ref([1, 0, 0]);

	const onChangeTabsState = (tab) => {
		tabsState.value.forEach((el, i) => {
			if (tab === i) tabsState.value[i] = 1;
			else tabsState.value[i] = 0;
		});
	};
</script>
<style scoped>
	.tab {
		padding: 50px 0;
	}

	.tab-options {
		justify-content: center;
		margin-bottom: 30px;
	}

	.btn-tab {
		font-weight: 500;
		background: none;
		border: none;
		border-bottom: 1px solid var(--grayishBlue);
		width: 280px;
		font-size: 18px;
		padding: 20px 0;
	}

	.btn-tab:hover {
		cursor: pointer;
		color: var(--softRed);
	}

	.active {
		border-bottom: 4px solid var(--softRed);
		padding-bottom: 17px;
	}

	.tab-content {
		padding: 20px 0 70px;
		height: 560px;
	}

	@media (max-width: 992px) {
		.tab-options {
			flex-direction: column;
		}

		.btn-tab {
			width: 100%;
			padding: 25px 0;
		}

		.tab-content {
			padding: 20px 0 0 0;
			height: auto;
		}
	}
</style>
