<script lang="ts">
  let counter = 0;

  function resetCounter() {
    counter = 0;
  }
</script>

<svelte:head>
  <title>Another page</title>
</svelte:head>

<div class="min-w-full min-h-screen bg-emerald-700">
  <div class="py-16 px-32">
    <div class="flex flex-row">
      <button
        class="border-2 border-black w-32 mx-6"
        on:click={() => counter++}
      >
        <h1 class="font-bold m-4 text-xl">Increment</h1>
      </button>
      <button
        class="border-2 border-black w-32 mx-6"
        on:click={() => resetCounter()}
      >
        <h1 class="font-bold m-4 text-xl">Reset</h1>
      </button>
      <h1 class="font-bold my-4 text-xl mx-6">{counter}</h1>
    </div>
  </div>
</div>
