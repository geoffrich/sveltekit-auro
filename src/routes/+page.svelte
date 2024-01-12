<script>
	import { onMount } from 'svelte';
	// this custom element is safe to import on server & client
	// it uses a newer version of lit that doesn't reference `window` at the top level of a script
	import './test-component';
	onMount(() => {
		// this component relies on an old version of lit that references `window` directly
		// we need to import it inside `onMount`, so that it's only imported on the client (where window is available)
		import('@aurodesignsystem/auro-button');
	});
</script>

<auro-button>Hello World</auro-button>
<simple-greeting></simple-greeting>
