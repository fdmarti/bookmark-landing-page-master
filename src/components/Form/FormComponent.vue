<template>
	<form @submit.prevent="onSubmitContact">
		<input
			type="email"
			placeholder="Enter your email address"
			v-model="email"
			:class="[
				{ hasErrors: hasErrors },
				{ hasCorrectFormat: hasCorrectFormat },
			]"
		/>
		<span class="error-msg" v-if="hasErrors">Make sure it's an email</span>
		<img
			class="icon-form"
			v-if="hasErrors"
			src="/images/icon-error.svg"
			alt="error icon form"
		/>
		<img
			class="icon-form"
			v-if="hasCorrectFormat"
			src="/images/icon-check.svg"
			alt="check icon form"
		/>
		<ButtonComponent text="Contact Us" color="softRed" />
	</form>
</template>

<script setup>
	import { ref } from 'vue';

	import './FormComponent.css';
	import { ButtonComponent } from '../UI';

	const email = ref('');
	const hasErrors = ref(false);
	const hasCorrectFormat = ref(false);
	const mailformat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;

	const onSubmitContact = () => {
		if (email.value.match(mailformat)) {
			hasErrors.value = false;
			hasCorrectFormat.value = true;
		} else {
			hasErrors.value = true;
			hasCorrectFormat.value = false;
		}
	};
</script>
