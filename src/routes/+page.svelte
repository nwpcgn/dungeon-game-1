<script lang="ts">
	import ListGroup from './ListGroup.svelte'

	let { data } = $props()
</script>

<header class="header">
	<div class="navbar bg-neutral text-neutral-content">
		<a href="#/" class="btn btn-neutral text-xl">{data.name}</a>
	</div>
</header>

<main class="main">
	<section class="nwp page-layer center" data-theme="retro">
		<ListGroup {...data}></ListGroup>
	</section>
</main>

