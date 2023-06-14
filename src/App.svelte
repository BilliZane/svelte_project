<script>
  import Hello from './components/Hello.svelte'
  import Reactive from './components/Reactive.svelte'
  import CatPic from './components/CatPic.svelte'
  import Playground from './components/Playground.svelte'
  import SomeForm from './components/SomeForm.svelte'
  import HTMLcode from './components/HTMLcode.svelte'
</script>

<main>
  <Hello />
  <Reactive />
  <CatPic />
  <Playground />
  <SomeForm />
  <HTMLcode />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  :global(h1) {
    color: #ff3e00;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
