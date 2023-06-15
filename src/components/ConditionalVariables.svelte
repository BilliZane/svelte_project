<script>
  let value = 'Hello'

  $: error = isValid(value)

  const isValid = () => value.length >= 5 && value.length <= 10
</script>

<h1>App</h1>

<input type="text" bind:value class:green={error} class:red={!error} />

{#if value.length < 5}
  <p>Длинна меньше 5 символов</p>
{:else if value.length > 10}
  <p>Длинна больше 10 символов</p>
{:else}
  <p>Длиннамежду 5 и 10 символов</p>
{/if}

<style>
  input {
    outline: none;
  }
  .red {
    border-color: red;
  }
  .green {
    border-color: green;
  }
</style>
