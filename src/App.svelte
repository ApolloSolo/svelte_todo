<script>
  import TodoContainer from "./components/Todo_Container.svelte";
</script>

<main>
  <h1>To-Do</h1>
  <p>Track Your Tasks</p>
  <TodoContainer />
</main>

<style>
  main {
    height: 100%;
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  p {
    color: rgb(0, 255, 255);
    font-size: 2rem;
  }

  h1 {
    color: rgb(0, 255, 255);
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
    font-size: 5.5rem;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
