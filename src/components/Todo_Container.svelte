<script>
  let edit = false;
  $: active_class = edit ? "checkbox" : "hidden";

  const show_edit = () => {
    edit = !edit;
  };

  const todos = [
    { title: "Go for run", complete_by: "02/18/23", complete: false },
    { title: "Walk frog", complete_by: "02/12/23", complete: false }
  ];
</script>

<section>
  <button class="edit" on:click={show_edit}>Edit</button>
  <div class="container">
    {#each todos as todo}
      <div class="inner-contain">
        <div class="title">
          <input class={active_class} type="checkbox" />
          <h3>{todo.title}</h3>
        </div>
        <div class="date">
          <h4>Complete By</h4>
          <p>{todo.complete_by}</p>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  section {
    margin-top: 2rem;
  }

  .edit {
    background-image: linear-gradient(rgb(0, 255, 255), rgb(0, 159, 159));
    border: 0;
    border-radius: 4px;
    box-shadow: rgba(0, 0, 0, 0.3) 0 5px 15px;
    box-sizing: border-box;
    color: rgb(0, 0, 0);
    cursor: pointer;
    font-family: Montserrat, sans-serif;
    font-size: 0.9em;
    margin: 5px;
    padding: 10px 15px;
    text-align: center;
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
  }

  .container {
    max-width: 750px;
    border: solid white 1px;
    border-radius: 0.25rem;
    margin: 0 auto;
  }

  .inner-contain {
    display: flex;
    justify-content: space-between;
    color: aliceblue;
    padding: 1rem;
  }

  .title {
    display: flex;
    align-items: center;
  }
  .checkbox {
    margin-right: 1rem;
    width: 20px;
    height: 20px;
  }

  .hidden {
    display: none;
  }

  .title h3 {
    font-size: 2.125rem;
  }

  .date h4 {
    font-size: 1.75rem;
  }

  .date p {
    font-size: 1.5rem;
  }
</style>
