<!-- 
    Reactive $: variable/blocks/function is used for reactivity;
    It's replaced by $derived() and, $effect()
-->

<script>
    let numbers = $state([1]);
	let count = $derived(numbers.length);
   
    let total, multiplication, output;

    $effect(()=>{
        total = numbers.reduce((t, n) => t + n, 0)
        multiplication = numbers.reduce((t, n) => t * n, 1);
        formatOutput(numbers, total,multiplication)
    });

    function formatOutput(numbers, total, multiplication){
        output = {
            total: `${numbers.join(' + ')} = ${total}`,
            multiplication: `${numbers.join(' * ')} = ${multiplication}`,
        }
    }

</script>

<button type="button" class="btn btn-primary" onclick={()=>numbers.push(count+1)}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

<p>Numbers are: {numbers.join(' , ')}</p>
<p>{output?.total}</p>
<p>{output?.multiplication}</p>