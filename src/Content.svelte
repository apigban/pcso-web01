<script>
  import Card from "./Card.svelte";
  let query = "";
  let result;

  async function getResult() {
    let response = await fetch(`http://192.168.0.117:8081/${query}`);
    let text = await response.text();
    let data = text;
    return data;
  }

  function submitHandler(e) {
    result = getResult();
  }
</script>

<div class="flex-1 container mt-5 bg-gray-200">
  <div class="row">
    <div class="col-md" />
    <div class="col-md-8 text-center">
      <h1 class="display-4">API</h1>
      <form class="form-inline" on:submit|preventDefault={submitHandler}>
        <input class="w-75 form-control" bind:value={query} />
        <button class="w-25 btn btn-dark">Submit</button>
      </form>

      {#if result === undefined}
        <p />
      {:else}
        {#await result}

          <p>Loading...</p>

        {:then value}
          {value}
        {:catch error}
          {error.message}
        {/await}
      {/if}
    </div>
    <div class="col-md" />
  </div>
</div>

{#if result === undefined}
  <p />
{:else}
  <p>Loading...</p>

  {#await result then value}

    <Card data={value} />

  {/await}
{/if}
