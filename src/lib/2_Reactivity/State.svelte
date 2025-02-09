<!-- 
    All let variable worked as reactive variable
    Reactivity triggered in assignment
-->

<script>
	let count = $state(0);
    let numbers = $state([]);

    function handleClick(){
        count++;
        numbers.push(count);
        //console.log(":::count :::",$state.snapshot(count), count); //$state.snapshot is a shallow copy of count;
    }

    //$inspect is a debugging tool, works with $state, $props, $derived, passed as multiple param
    $inspect(numbers).with((type,numbersCurrentValue)=>{
        console.log(type,numbersCurrentValue);
        console.trace();
    }); 

</script>

<button type="button" class="btn btn-primary" onclick={handleClick}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

<p>Numbers are: {numbers.join(' , ')}</p>