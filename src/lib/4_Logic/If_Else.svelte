<script>
  const number1 = 5;
  const number2 = 7;
</script>

<!-- ::: Example of If Block :::: -->
{#if number1 > number2}
  <p>{number1} is greater than {number2}</p>
{/if}

<!-- ::: Example of If-Else Block :::: -->
{#if number1 > number2}
  <p>{number1} is greater than {number2}</p>
{:else}
  <p>{number1} is not greater to {number2}</p>
{/if}

<!-- ::: Example of If-Else If-Else Block :::: -->
{#if number1 > number2}
  <p>{number1} is greater than {number2}</p>
{:else if number1 < number2}
  <p>{number1} is less than {number2}</p>
{:else}
  <p>{number1} is equal to {number2}</p>
{/if}
