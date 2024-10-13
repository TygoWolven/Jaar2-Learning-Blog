<script lang="ts">
	import * as config from '$lib/config'
	import { Github, Instagram, Linkedin } from 'lucide-svelte'
</script>

<!-- Footer -->
<footer>
	<p>{config.title} &copy {new Date().getFullYear()}</p>
	<ul class="socials">
		<li>
			<a href="https://github.com/TygoWolven"><Github />Github</a>
		</li>
		<li>
			<a href="https://www.instagram.com/tygowolvenn_/"><Instagram />Instagram</a>
		</li>
		<li>
			<a href="https://www.linkedin.com/in/tygo-wolven-091515241/"><Linkedin />Linkedin</a>
		</li>
	</ul>
</footer>

<style>
	footer {
		display: flex;
		justify-content: space-between;
		padding-block: var(--size-7);
		border-top: 1px solid var(--border);
	}

	.socials {
		display: flex;
		align-items: center;
		gap: 2rem;
	}

	a {
		display: flex;
		gap: 0.5rem;
	}

	p, a {
		color: var(--text-2);
	}

	@media (max-width: 768px) {
		footer {
			width: 100vw;
			flex-direction: column;
			text-align: left;
		}

		.socials {
			flex-direction: column;
			align-items: start;
			gap: 1em;
		}

		p {
			margin-bottom: 1em;
		}
	}
</style>
