<script>
	import Modal from '$lib/Modal.svelte';
	let isOpen1 = false;
	let isOpen2 = false;
</script>

<button
	class="inline-flex items-center px-2.5 py-1.5 border border-transparent text-xs font-medium rounded text-indigo-700 bg-indigo-100 hover:bg-indigo-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
	on:click={() => {
		isOpen1 = true;
	}}>Open good modal</button
>
<button
	class="inline-flex items-center justify-center rounded-md border border-transparent bg-red-100 px-4 py-2 font-medium text-red-700 hover:bg-red-200 focus:outline-none focus:ring-2 focus:ring-red-500 focus:ring-offset-2 sm:text-sm"
	on:click={() => {
		isOpen2 = true;
	}}>Open bad modal</button
>
<!-- This modal behaves as expected -->
<!-- It dissapears when clicking the navigateAway button -->
<Modal bind:isOpen={isOpen1} />

<!-- ################## -->

<!-- This does not behave as expected -->
<!-- It does not disappear when clicking the navigateAway button. It also becomes unresponsive. -->
<div>
	<Modal bind:isOpen={isOpen2} />
</div>
