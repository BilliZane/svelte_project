<script>
  let name = 'Svelte'
  let agree = true
  let text = 'text'
  let select = 'Apple'

  let sex = 'male'
</script>

<div class="binding">
  <h1>{name}</h1>
  <input type="text" bind:value={name} />
  <hr />

  <input type="checkbox" bind:checked={agree} />
  {agree}
  <hr />

  <p>{text}</p>
  <textarea bind:value={text} />
  <hr />

  <select name="select" bind:value={select}>
    <option value="Apple">Apple</option>
    <option value="Orange">Orange</option>
    <option value="Banana">Banana</option>
  </select>
  <hr />

  <input type="radio" value="male" bind:group={sex} />male
  <input type="radio" value="female" bind:group={sex} />female
  <br />{sex}
</div>

<style>
  .binding {
    border: solid 1px #252525;
  }
</style>
