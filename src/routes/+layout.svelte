<script lang="ts">
	import '../app.css'
	import '../assets/scss/index.scss'
	import { Sprites } from '$lib'
	let { children } = $props()
</script>

{@render children()}

<Sprites></Sprites>
