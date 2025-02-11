<script>
	let m = $state({ x: 0, y: 0 });

	function onpointermove(event) {
		m.x = event.clientX;
		m.y = event.clientY;
	}
   
</script>

<div class="bg-primary p-5" on:pointermove={onpointermove}>
    The pointer is at {m.x} x {m.y}
</div>

