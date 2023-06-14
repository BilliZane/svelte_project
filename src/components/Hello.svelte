<script>
  import { firstLetterToUpperCase } from '../composables/firstLetterToUpperCase'

  let name = 'john'

  const changeNameHandler = () => (name = 'Mitchell')
</script>

<div class="hello">
  <h1>Hello {firstLetterToUpperCase(name)}!</h1>
  <button on:click={changeNameHandler}>Change name</button>
</div>

<style>
  .hello {
    border: solid 1px rgb(179, 66, 66);
  }
</style>
