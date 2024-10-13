<script lang="ts">
	import { formatDate } from '$lib/utils'
	import * as config from '$lib/config'

	export let data
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<!-- Information -->
<section id="Documentation">
	<h2>Sprints</h2>
	<ul class="posts">
		{#each data.posts as post}
			{#if post.value === 1}
				<li class="post">
					<a href={post.slug} class="title">{post.title}</a>
					<p class="date">{formatDate(post.date)}</p>
					<p class="description">{post.description}</p>
				</li>
			{/if}
		{/each}
	</ul>

	<h2>We Love Webs</h2>
	<ul class="posts">
		{#each data.posts as post}
			{#if post.value === 2}
				<li class="post">
					<a href={post.slug} class="title">{post.title}</a>
					<p class="date">{formatDate(post.date)}</p>
					<p class="description">{post.description}</p>
				</li>
			{/if}
		{/each}
	</ul>
</section>

<style>
	section {
		height: fit-content;
	}

	.posts {
		display: flex;
		flex-wrap: wrap;
		gap: 2rem;
	}

	.post {
		max-width: 25em;
		max-inline-size: var(--size-content-3);
	}

	.post:not(:last-child) {
		border-right: 1px solid var(--border);
		padding-right: var(--size-7);
	}

	.title {
		font-size: var(--font-size-fluid-2);
		text-transform: capitalize;
	}

	.date {
		color: var(--text-2);
	}

	.description {
		margin-top: var(--size-3);
	}

	h2 {
		font-size: 3.5em;
	}

	h2:not(:first-child) {
		margin-top: 1.5em;
	}
</style>

