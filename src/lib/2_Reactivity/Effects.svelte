<!-- 
    Reactive $: variable/blocks/function is used for reactivity;
    It's replaced by $derived() and, $effect()
-->

<script>
	let count = 1;
    $: numbers = [...(numbers||[]), count];

    let total, multiplication, output = {};

    $:{
        total = numbers.reduce((t, n) => t + n, 0)
        multiplication = numbers.reduce((t, n) => t * n, 1)
    }

    function formatOutput(numbers, total, multiplication){
        output = {
            total: `${numbers.join(' + ')} = ${total}`,
            multiplication: `${numbers.join(' * ')} = ${multiplication}`,
        }
        console.log(output);
    }

    $: formatOutput(numbers, total,multiplication);

</script>

<button type="button" class="btn btn-primary" onclick={()=>count++}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

<p>Numbers are: {numbers.join(' , ')}</p>
<p>{output.total}</p>
<p>{output.multiplication}</p>