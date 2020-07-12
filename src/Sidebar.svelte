<script>
  export let displayResult = false;
  function toggleResult() {
    displayResult = !displayResult;
  }
  let title = "PCSO API";
</script>

<div class="w-1/5 h-screen bg-gray-400">
  <div class="flex items-center justify-center mt-10">
    <h1>{title}</h1>
  </div>

  <nav class="mt-10">
    <a
      class="flex items-center py-2 px-8 block bg-gray-200 text-gray-700"
      href="#">
      <span class="mx-4 font-medium" on:click={toggleResult}>Game Results</span>
    </a>
    {#if displayResult}
      <h4>amount : "asdasd"</h4>
    {/if}
    <a
      class="flex items-center mt-5 py-2 px-8 block text-gray-600 border-r-4
      border-white hover:bg-gray-200 hover:text-gray-700 hover:border-gray-700"
      href="#">
      <span class="mx-4 font-medium">About</span>
    </a>
  </nav>
</div>
