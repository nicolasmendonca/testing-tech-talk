<script lang="ts">
	import { onDestroy, onMount } from 'svelte'

	import Reveal from 'reveal.js'
	import Highlight from 'reveal.js/plugin/highlight/highlight'
	import Markdown from 'reveal.js/plugin/markdown/markdown'
	import Notes from 'reveal.js/plugin/notes/notes'

	import 'reveal.js/dist/reveal.css'
	import 'reveal.js/dist/theme/black.css'
	import 'reveal.js/plugin/highlight/monokai.css'

	import Presentation from './presentation.svelte'

	let deck: Reveal.Api | undefined

	onMount(() => {
		deck = new Reveal({
			plugins: [Markdown, Highlight, Notes],
			autoAnimateEasing: 'ease',
			autoAnimateDuration: 1,
			hash: true
			// controls: false,
			// progress: false
		})

		deck.initialize()
	})

	onDestroy(() => {
		deck?.destroy()
		deck = undefined
	})
</script>

<div class="reveal">
	<div class="slides">
		{#if deck}
			<Presentation />
		{/if}
	</div>
</div>
