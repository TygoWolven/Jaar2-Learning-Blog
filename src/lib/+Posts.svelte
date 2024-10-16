<script lang="ts">
	import { CircleCheck, CircleX } from 'lucide-svelte'
</script>

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