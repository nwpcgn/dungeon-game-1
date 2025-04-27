<script lang="ts">
	let { menu = [], label = 'Game Navigation' } = $props()
</script>

<div class="rounded-box w-[360px] border bg-amber-600 p-3">
	<ul class="list bg-base-100 rounded-box shadow-md">
		<li class="p-4 pb-2 text-xs tracking-wide opacity-60">{label}</li>
		{#each menu as { name, title, href, icon, avatar, image }}
			{#if href !== '/'}
				<li class="list-row">
					<button class="btn btn-circle">
						<img class="rounded-box size-8" src={image} />
					</button>
					<div>
						<div>{name}</div>
						<div class="text-xs font-semibold uppercase opacity-60">
							{title}
						</div>
					</div>
					<a href="#{href}" class="btn btn-circle btn-neutral btn-outline">
						{@render iconT(icon)}
					</a>
				</li>
			{/if}
		{/each}
	</ul>
</div>

{#snippet iconT(name)}
	<svg class="icon-game" style="--fs: 32px;"
		><use xlink:href="#{name}"></use></svg>
{/snippet}
