<script>
	import './test-component';
	import '@aurodesignsystem/auro-alert';
	import '@aurodesignsystem/auro-checkbox';
</script>

<auro-alert type="error">Transaction failed.</auro-alert>

<auro-checkbox-group>
	<span slot="legend">Form label goes here</span>
	<auro-checkbox value="checkbox option" name="example1" id="checkbox-basic1"
		>Checkbox option</auro-checkbox
	>
	<auro-checkbox value="checkbox option" name="example2" id="checkbox-basic2" checked
		>Checkbox option</auro-checkbox
	>
	<auro-checkbox value="checkbox option" name="example3" id="checkbox-basic3"
		>Checkbox option</auro-checkbox
	>
	<auro-checkbox value="checkbox option" name="example4" id="checkbox-basic4"
		>Checkbox option</auro-checkbox
	>
</auro-checkbox-group>
