<!-- 
    All let variable worked as reactive variable
    Reactivity triggered in assignment
-->

<script>
	let count = 0;
    let numbers = [];

    function handleClick(){
        count++;
        numbers.push(count);
        numbers = numbers;
    }
</script>

<button type="button" class="btn btn-primary" onclick={handleClick}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

<p>Numbers are: {numbers.join(' , ')}</p>