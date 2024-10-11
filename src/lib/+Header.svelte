<script lang="ts">
	import * as config from '$lib/config'
	import Toggle from '$lib/+Toggle.svelte'
	import { House } from 'lucide-svelte'

</script>

<nav>
  <!-- Title -->
	<a href="/" class="title">
		<b>{config.title}</b>
		<House />
	</a>

  <!-- Navigation -->
	<ul class="links">
		<li>
			<a href="/about">About</a>
		</li>
		<li>
			<a href="/contact">Contact</a>
		</li>
	</ul>

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

	.links {
		margin-block: var(--size-7);
	}

	@media (min-width: 768px) {
		nav {
			display: flex;
			justify-content: space-between;
		}

		.links {
			display: flex;
			gap: var(--size-7);
			margin-block: 0;
		}
	}
</style>
