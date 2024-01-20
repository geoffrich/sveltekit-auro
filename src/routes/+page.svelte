<script>
	import { onMount } from 'svelte';
	// this custom element is safe to import on server & client
	// it uses a newer version of lit that doesn't reference `window` at the top level of a script
	import './test-component';
	import('@aurodesignsystem/auro-alert');
	onMount(() => {
		// this component relies on an old version of lit that references `window` directly
		// we need to import it inside `onMount`, so that it's only imported on the client (where window is available)
		import('@aurodesignsystem/auro-checkbox');
		// import('@aurodesignsystem/auro-alert');
	});
</script>

<auro-alert type="error">Transaction failed.</auro-alert>

<auro-checkbox-group>
  <span slot="legend">Form label goes here</span>
  <auro-checkbox value="checkbox option" name="example1" id="checkbox-basic1">Checkbox option</auro-checkbox>
  <auro-checkbox value="checkbox option" name="example2" id="checkbox-basic2" checked>Checkbox option</auro-checkbox>
  <auro-checkbox value="checkbox option" name="example3" id="checkbox-basic3">Checkbox option</auro-checkbox>
  <auro-checkbox value="checkbox option" name="example4" id="checkbox-basic4">Checkbox option</auro-checkbox>
</auro-checkbox-group>
