<script lang="ts">
  import { goto } from "$app/navigation";

  let showMenu = false;

  function onClickNavigate(path: string): void {
    showMenu = false;
    goto(path);
  }
</script>

{#if showMenu}
  <div class="flex flex-row">
    <button
      class="h-screen lg:w-[60vw] w-0"
      on:click={() => (showMenu = !showMenu)}
    />
    <nav
      class="bg-green-300 flex flex-col h-screen lg:w-[40vw] w-screen flex-none"
    >
      <button on:click={() => (showMenu = !showMenu)} class="w-12 h-12 m-5">
        <img src="menu.png" alt="hamburger" />
      </button>

      <button on:click={() => onClickNavigate("/")} class=""> Home </button>
      <button on:click={() => onClickNavigate("/anotherPage")}>
        Another Page
      </button>
    </nav>
  </div>
{:else}
  <nav class="bg-opacity-0">
    <button on:click={() => (showMenu = !showMenu)} class="w-12 h-12 m-5">
      <img src="menu.png" alt="hamburger" />
    </button>
  </nav>
{/if}
