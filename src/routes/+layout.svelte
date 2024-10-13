<script lang="ts">
	import Footer from '$lib/+Footer.svelte'
	import Header from '$lib/+Header.svelte'
	import 'open-props/style'
	import 'open-props/normalize'
	import 'open-props/buttons'
	import '../app.css'
</script>

<div class="layout">
  <!-- Header -->
	<Header />

	<main>
		<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" version="1.1">
			<defs> 
				<linearGradient id="sw-gradient" x1="0" x2="1" y1="1" y2="0">
					<stop id="stop1" stop-color="rgba(125, 250, 125, 1)" offset="0%"></stop>
					<stop id="stop2" stop-color="rgba(125, 250, 125, 1)" offset="100%"></stop>
				</linearGradient>
			</defs>
			<path fill="none" d="M13.5,-18.5C19.8,-14,28.8,-13.2,33,-8.7C37.2,-4.3,36.6,3.7,31.6,7.6C26.6,11.5,17.3,11.2,11.3,12.5C5.3,13.8,2.7,16.6,-1.2,18.3C-5,19.9,-10,20.3,-15.5,18.8C-20.9,17.3,-26.7,14,-30.4,8.5C-34,3.1,-35.4,-4.4,-33.6,-11.2C-31.8,-18,-26.8,-24.1,-20.7,-28.5C-14.6,-33,-7.3,-35.9,-1.8,-33.4C3.6,-30.9,7.2,-22.9,13.5,-18.5Z" width="100%" height="100%" transform="translate(50 50)" stroke-width="1" style="transition: 0.3s;" stroke="url(#sw-gradient)"></path>
		</svg>

		<slot />
	</main>

  <!-- Footer -->
	<Footer />
</div>

<style>
	svg {
		filter: blur(100px);
		width: max-content;
		position: fixed;
		z-index: -10;
	}

	.layout {
		height: 100%;
		max-inline-size: 1440px;
		display: grid;
		grid-template-rows: auto 1fr auto;
		margin-inline: auto;
		padding-inline: var(--size-7);
	}

	main {
		padding-block: var(--size-9);
	}

	@media (min-width: 1440px) {
		.layout {
			padding-inline: 0;
		}
	}
</style>
