<script>
  export let name = 'John'
  export let age = 23
  export let job = 'Developer'
</script>

<div>
  <p>Имя: <b>{name}</b></p>
  <p>Возраст: <b>{age}</b></p>
  <p>Работа: <b>{job}</b></p>

  {#if age < 18}
    <p>Пиво продавать нельзя</p>
  {:else}
    <p>Можно продавать</p>
  {/if}
</div>

<style>
  div {
    border: solid 1px red;
    padding: 1rem;
    margin-bottom: 1rem;
  }
</style>
