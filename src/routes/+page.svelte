<script lang="ts">
	import { formatDate } from '$lib/utils'
	import * as config from '$lib/config'
	import { CircleCheck, CircleX } from 'lucide-svelte'
	export let data
</script>

<section id="Home">
	<h1>Learning Blog</h1>
	<p>
		Welkom in mijn blog! Je zult hier mijn documentatie vinden van de opleiding Frontend Design & 
		Development. Denk hierbij aan zowel colleges, als presentaties van gastsprekers uit het vakgebied.
	</p>
	<a href="#Documentation">Ontdek meer</a>
</section>

<!-- Information -->
<section id="Documentation">
	<h2>Sprints</h2>
	<ul class="posts">
		{#each data.posts as post}
			{#if post.value === 1}
				<li class="post">
					<a href={post.slug} class="title">{post.title}</a>
					<div>
						<p class="date">{formatDate(post.date)}</p>
						{#if post.status === true}
							<p class="status true">Up to date <span><CircleCheck /></span></p>
						{:else}
							<p class="status false">Work in progress <span><CircleX /></span></p>
						{/if}
					</div>
					<p class="description">{post.description}</p>
				</li>
			{/if}
		{/each}
	</ul>

	<h2>Gastsprekers</h2>
	<ul class="posts">
		{#each data.posts as post}
			{#if post.value === 2}
				<li class="post">
					<a href={post.slug} class="title">{post.title}</a>
					<div>
						<p class="date">{formatDate(post.date)}</p>
						{#if post.status === true}
							<p class="status true">Up to date <span><CircleCheck /></span></p>
						{:else}
							<p class="status false">Work in progress <span><CircleX /></span></p>
						{/if}
					</div>
					<p class="description">{post.description}</p>
				</li>
			{/if}
		{/each}
	</ul>

	<h2>Experimenten</h2>
	<ul class="posts">
		{#each data.posts as post}
			{#if post.value === 3}
				<li class="post">
					<a href={post.slug} class="title">{post.title}</a>
					<div>
						<p class="date">{formatDate(post.date)}</p>
						{#if post.status === true}
							<p class="status true">Up to date <span><CircleCheck /></span></p>
						{:else}
							<p class="status false">Work in progress <span><CircleX /></span></p>
						{/if}
					</div>
					<p class="description">{post.description}</p>
				</li>
			{/if}
		{/each}
	</ul>
</section>

<style>
	#Home {
		display: flex;
		flex-direction: column;
		height: 60vh;
	}

	h1 {
		text-transform: uppercase;
		margin-top: 0.5em;
		font-size: 10vw;
	}

	h1 + p {
		max-inline-size: 85vw;
	}

	#Home a {
		color: #DEE2E6;
		background: var(--brand-light);
		border: 5px solid var(--brand-dark);
		padding: 0.5em 1em;
		margin-top: 2em;

		border-radius: 3em;
		transition: 0.5s ease;
		text-decoration: none;
		width: fit-content;
	}

	#Home a:hover {
		padding: 0.5em 2.5em;
		box-shadow: 0 0 50px 5px var(--brand);
	}

	.posts {
		display: flex;
		flex-wrap: wrap;
		gap: 2rem;
	}

	.post {
		width: 25em;
		border-right: 1px solid var(--border);
		padding-right: var(--size-7);
	}

	.post a {
		line-height: 1em;
	}

	.post div {
		display: flex;
		justify-content: space-between;
	}

	.post div p {
		display: flex;
		gap: 0.5em;
	}

	.status.true span {
		color: var(--brand);
	}

	.status.false span {
		color: rgb(175, 0, 0);
	}

	.title {
		font-size: var(--font-size-fluid-2);
		text-transform: capitalize;
	}

	.date,
	.status {
		color: var(--text-2);
	}

	.description {
		margin-top: var(--size-3);
	}

	h2 {
		font-size: var(--font-size-fluid-3);
	}

	h2:not(:first-child) {
		margin-top: 1.5em;
	}

	@media (min-width: 768px) {
		#Home {
			align-items: center;
		}

		h1 {
			font-size: 5em;
		}

		h1 + p {
			text-align: center;
			max-inline-size: var(--size-content-3);
		}
	}

	@media (max-width: 65em) {
		.post {
			max-width: unset;
			width: 90vw;
		}
	}
</style>

