<script>
	import Modal from '$lib/Modal.svelte';
	let isOpen = false;
</script>

<button
	on:click={() => {
		isOpen = true;
	}}>Open</button
>

<!-- This modal behaves as expected -->
<!-- It dissapears when clicking the navigateAway button -->
<Modal bind:isOpen />

<!-- ################## -->

<!-- This does not behave as expected -->
<!-- It does not disappear when clicking the navigateAway button -->
<!-- don't forget to comment out the first modal before uncommenting the second -->
<!-- <div>
	<Modal bind:isOpen />
</div> -->
