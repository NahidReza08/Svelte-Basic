<script>
    import Counter from './Counter.svelte';
    import { numbers } from './state.svelte.js';
</script>

<Counter />
<p>Numbers outside counter are: {numbers.join(' , ')}</p>
