<script>
	import { numbers } from './state.svelte.js';
    let count = $derived(numbers.length);
</script>
<button type="button" class="btn btn-primary" onclick={()=>numbers.push(count+1)}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>
<p>Numbers inside counter are: {numbers.join(' , ')}</p>
