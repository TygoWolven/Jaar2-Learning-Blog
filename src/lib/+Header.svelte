<script lang="ts">
	import * as config from '$lib/config'
	import Toggle from '$lib/+Toggle.svelte'
	import Logo from "$lib/assets/TSW-Logo.png"
</script>

<nav>
  <!-- Home Button -->
	<a href="/" class="logo">
		<img alt="Brand Logo" src={Logo} />
	</a>
  <!-- Theme -->
  <Toggle />
</nav>

<style>
	nav {
		padding-block: var(--size-7);
	}

	nav > a {
		display: flex;
		gap: var(--size-2);
	}

	a {
		color: inherit;
		text-decoration: none;
	}

	.logo > img {
		height: 30px;
		border-radius: unset;
	}

	@media (min-width: 768px) {
		nav {
			display: flex;
			justify-content: space-between;
		}
	}
</style>
