<template>
	<nav class="flex-center width-max">
		<div class="logo">
			<img src="/images/logo-bookmark.svg" alt="bookmark logo" />
		</div>
		<ul class="menu flex-center">
			<li class="menu-item">Features</li>
			<li class="menu-item">Pricing</li>
			<li class="menu-item">Contact</li>
			<li class="menu-item">
				<ButtonComponent text="Login" color="softRed" :upper="true" />
			</li>
		</ul>
		<img
			class="toggle-menu"
			src="/images/icon-hamburger.svg"
			alt="hamburger icon menu"
			@click="onClickShowMenu"
		/>
	</nav>
</template>
<script setup>
	import ButtonComponent from './UI/ButtonComponent.vue';

	const onClickShowMenu = () => {
		const menu = document.querySelector('.menu');
		menu.classList.toggle('show');

		const imageMenu = document.querySelector('.toggle-menu');

		if (menu.classList.contains('show')) {
			imageMenu.src = '/images/icon-close.svg';
			document.body.style.overflow = 'hidden';
		} else {
			imageMenu.src = '/images/icon-hamburger.svg';
			document.body.style.overflow = 'auto';
		}
	};
</script>
<style scoped>
	nav {
		justify-content: space-between;
		padding: 40px 20px;
	}

	.toggle-menu {
		display: none;
		width: 25px;
		padding-right: 20px;
		z-index: 3;
	}

	.menu {
		gap: 5rem;
	}

	.menu-item {
		text-transform: uppercase;
		font-size: 14px;
	}

	.menu-item:hover {
		cursor: pointer;
		color: var(--softRed);
	}

	@media (max-width: 768px) {
		.menu {
			display: none;

			background-color: #02263de0;
			position: absolute;
			top: 0;
			left: 0;
			width: 100%;
			height: 100vh;
			z-index: 2;
		}

		.menu-item {
			position: relative;
			top: 130px;
			text-align: center;
			color: var(--white);
			font-size: 18px;
			width: 80%;
			padding-bottom: 15px;
			border-bottom: 1px solid var(--grayishBlue);
		}

		.menu-item:last-child {
			border: none;
		}

		.menu-item .btn {
			width: 100%;
		}

		.show {
			display: flex;
			align-items: center;
			flex-direction: column;
			gap: 3rem;
		}

		.toggle-menu {
			display: block;
		}
	}
</style>
