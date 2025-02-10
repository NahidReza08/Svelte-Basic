<script>
  const number1 = 5;
  const number2 = 7;
</script>

{#if number1 > number2}
  <p>{number1} is greater than {number2}</p>
{:else if number1 < number2}
  <p>{number1} is less than {number2}</p>
{:else}
  <p>{number1} is equal to {number2}</p>
{/if}
