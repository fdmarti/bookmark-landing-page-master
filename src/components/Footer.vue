<template>
	<footer class="flex-center">
		<div class="menu-footer flex-center">
			<img
				@click="onClickLogo"
				src="/images/logo-bookmark-white.svg"
				alt="bookmark logo white footer"
			/>
			<ul class="menu-footer flex-center">
				<li class="menu-footer-item">Features</li>
				<li class="menu-footer-item">Pricing</li>
				<li class="menu-footer-item">Contact</li>
			</ul>
		</div>
		<div class="social-media flex-center">
			<a href="https://www.linkedin.com/in/fededmartinez/" target="_blank">
				<img src="/images/icon-linkedin.svg" alt="linkedin logo" />
			</a>
			<a href="https://github.com/fdmarti" target="_blank"
				><img src="/images/icon-github.svg" alt="github logo white footer"
			/></a>
		</div>
	</footer>
</template>
<script setup>
	const onClickLogo = () => {
		window.scrollTo({ top: 0, behavior: 'smooth' });
	};
</script>
<style scoped>
	footer {
		background-color: var(--darkBlue);
		justify-content: space-around;
		padding: 15px 20px;
	}

	.menu-footer {
		gap: 3rem;
	}

	.menu-footer-item {
		color: var(--white);
		text-transform: uppercase;
		font-size: 14px;
	}

	.menu-footer-item:hover,
	.social-media img:hover {
		cursor: pointer;
		color: var(--softRed);
	}

	img:hover {
		cursor: pointer;
	}

	.social-media {
		gap: 2rem;
	}

	.social-media img {
		width: 30px;
	}

	@media (max-width: 768px) {
		footer {
			padding: 40px 0;
			flex-direction: column;
			gap: 2rem;
		}

		.menu-footer {
			flex-direction: column;
			gap: 2rem;
		}
	}
</style>
