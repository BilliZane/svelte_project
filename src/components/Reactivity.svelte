<script>
  let name = 'Paul'
  let counter = 0

  $: counterClass = counter % 2 === 0 ? 'red' : 'blue'

  $: upperName = name.toUpperCase() //  some like computed in Vue
  $: lowername = name.toLocaleLowerCase() // some like computed in Vue

  $: {
    console.log('Name:', name)
    console.log('Counter:', counter)
  }

  $: if (counter === 10) {
    name = 'Counter is equal 10.'
  }

  const changeName = () => (name = 'Mitchell')
</script>

<div class="reactivity">
  <h2 class="reactivity__name">{name}</h2>
  <h2>{upperName}</h2>
  <h2>{lowername}</h2>
  <button on:click={changeName}>Change name</button>

  <!-- dynamic class -->
  <h1 class={counterClass}>{counter}</h1>
  <button on:click={() => counter++}>Plus</button>
</div>

<style>
  .reactivity {
    border: solid 1px magenta;
    font-weight: bold;
  }
  .red {
    color: red;
  }
  .blue {
    color: blue;
  }
</style>
