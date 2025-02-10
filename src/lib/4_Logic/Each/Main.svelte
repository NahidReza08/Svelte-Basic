<script>
	import Emoji from './Emoji.svelte';

	let things = $state([
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'carrot' },
		{ id: 4, name: 'doughnut' },
		{ id: 5, name: 'egg' }
	]);
</script>

<!-- Example of each block -->
{#each things as thing, index}
	({index}) id: {thing.id}, name: {thing.name} <br>
{/each}
<br>

<button type="button" class="btn btn-primary" onclick={() => things.shift()}>
	Remove first thing
</button>
<br><br>

<!-- 
    Without key, each add/removes the last component and update the others;
    All value directly involved to $props() updated, but rest are not modified. 
    Assign an unique key can solve the issue;
-->

<!-- Example of keyed each block -->
{#each things as thing (thing.id)}
	<Emoji name={thing.name} />
{/each}