<script>
  import Hello from './components/Hello.svelte'
  import Reactive from './components/Reactive.svelte'
  import CatPic from './components/CatPic.svelte'
  import Playground from './components/Playground.svelte'
  import SomeForm from './components/SomeForm.svelte'
  import HTMLcode from './components/HTMLcode.svelte'
  import Reactivity from './components/Reactivity.svelte'
  import TwoWayBindin from './components/TwoWayBindin.svelte'
  import ConditionalVariables from './components/ConditionalVariables.svelte'
  import PersonsList from './components/PersonsList.svelte'
  import Person from './components/Person.svelte'

  const people = [
    { id: 1, name: 'John', age: 23, job: 'Developer' },
    { id: 2, name: 'Paul', age: 17, job: 'Cleaner' },
  ]

  let name = 'Johny'
  let age = 30
  let jobTitle = 'Seller'
</script>

<main>
  <Hello />
  <Reactive />
  <CatPic />
  <Playground />
  <SomeForm />
  <HTMLcode />
  <Reactivity />
  <TwoWayBindin />
  <ConditionalVariables />
  
  <Person name={people[0].name} age={people[0].age} job={people[0].job} />
  <Person name={people[1].name} age={people[1].age} job={people[1].job} />
  <Person {name} {age} job={jobTitle} />
  <Person {...people[0]} />
  
  <PersonsList />
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
