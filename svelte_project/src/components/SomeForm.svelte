<script>
  let inputValue = ''

  const submithandler = () => {
    console.log(inputValue)
  }

  const clearInput = () => (inputValue = '')
</script>

<div class="form-wrap">
  <form on:submit|preventDefault={submithandler}>
    <input type="text" value={inputValue} on:input={(event) => (inputValue = event.target.value)} />
    <button type="submit">Submit form</button>
  </form>
  <button on:click={clearInput}>Clear</button>
</div>

<style>
  .form-wrap {
    border: solid 1px #88b207;
  }
</style>
