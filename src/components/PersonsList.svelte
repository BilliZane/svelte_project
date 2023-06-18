<script>
  import Person from './Person.svelte'

  let value = ''
  let people = [
    { id: 1, name: 'John', age: 23, job: 'Developer' },
    { id: 2, name: 'Paul', age: 17, job: 'Cleaner' },
    { id: 3, name: 'Emma', age: 30, job: 'Manager' },
    { id: 4, name: 'Sophia', age: 25, job: 'Designer' },
    { id: 5, name: 'Michael', age: 31, job: 'Engineer' },
    { id: 6, name: 'Olivia', age: 28, job: 'Teacher' },
    { id: 7, name: 'William', age: 19, job: 'Student' },
    { id: 8, name: 'Ava', age: 22, job: 'Writer' },
    { id: 9, name: 'James', age: 26, job: 'Programmer' },
    { id: 10, name: 'Isabella', age: 24, job: 'Artist' },
    { id: 11, name: 'Daniel', age: 29, job: 'Architect' },
    { id: 12, name: 'Mia', age: 20, job: 'Photographer' },
    { id: 13, name: 'Alexander', age: 27, job: 'Musician' },
    { id: 14, name: 'Ella', age: 18, job: 'Cashier' },
    { id: 15, name: 'Matthew', age: 32, job: 'Lawyer' },
    { id: 16, name: 'Sofia', age: 21, job: 'Dancer' },
    { id: 17, name: 'Andrew', age: 33, job: 'Chef' },
    { id: 18, name: 'Charlotte', age: 16, job: 'Waitress' },
    { id: 19, name: 'David', age: 34, job: 'Salesperson' },
    { id: 20, name: 'Abigail', age: 35, job: 'Consultant' },
  ]

  const addperson = () => {
    // people = people.concat([
    //   {
    //     id: Date.now(),
    //     name: value,
    //   },
    // ])

    people = [
      {
        id: Date.now(),
        name: value,
      },
      ...people,
    ]

    value = ''
  }

  const removeFirst = () => {
    people = people.slice(1)
  }
</script>

<h1>People's List</h1>
<input type="text" bind:value />
<button on:click={addperson}>Add person</button>
<button on:click={removeFirst}>Remove first</button>

<hr />
<!-- {#each people as person, i, (person.id)}
  <b>{person.id}</b><Person name={person.name} age={person.age} job={person.job} />
{/each} -->

{#each people as { id, name, age, job }, i (id)}
  <b>{i + 1}</b><Person {name} {age} {job} />
{:else}
  <p>No people!</p>
{/each}
