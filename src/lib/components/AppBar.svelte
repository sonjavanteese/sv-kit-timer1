<script>
  import { page } from "$app/stores";
  import Icon from "./Icon.svelte";
  import { user } from "../stores";
  export let name = "Nwp-App";
  export let size = 30;
  export let open = false;
  export let toggle = () => {
    open = !open;
  };
  $: currentPage = $page.url.pathname;
</script>

<svg aria-hidden="true" style="position: absolute; width: 0; height: 0; overflow: hidden;" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><defs><symbol id="icon-close" viewBox="0 0 28 28"><title>close</title><path d="M22.148 7.492l-6.508 6.508 6.508 6.508-1.641 1.641-6.508-6.508-6.508 6.508-1.641-1.641 6.508-6.508-6.508-6.508 1.641-1.641 6.508 6.508 6.508-6.508z"></path></symbol><symbol id="icon-drag" viewBox="0 0 28 28"><title>drag</title><path d="M4.648 17.5v-2.352h18.703v2.352h-18.703zM23.352 10.5v2.352h-18.703v-2.352h18.703z"></path></symbol><symbol id="icon-left" viewBox="0 0 28 28"><title>left</title><path d="M23.352 12.852v2.297h-14.219l6.508 6.563-1.641 1.641-9.352-9.352 9.352-9.352 1.641 1.641-6.508 6.563h14.219z"></path></symbol><symbol id="icon-menu" viewBox="0 0 28 28"><title>menu</title><path d="M3.5 7h21v2.352h-21v-2.352zM3.5 15.148v-2.297h21v2.297h-21zM3.5 21v-2.352h21v2.352h-21z"></path></symbol><symbol id="icon-more" viewBox="0 0 28 28"><title>more</title><path d="M14 18.648q0.93 0 1.641 0.711t0.711 1.641-0.711 1.641-1.641 0.711-1.641-0.711-0.711-1.641 0.711-1.641 1.641-0.711zM14 11.648q0.93 0 1.641 0.711t0.711 1.641-0.711 1.641-1.641 0.711-1.641-0.711-0.711-1.641 0.711-1.641 1.641-0.711zM14 9.352q-0.93 0-1.641-0.711t-0.711-1.641 0.711-1.641 1.641-0.711 1.641 0.711 0.711 1.641-0.711 1.641-1.641 0.711z"></path></symbol><symbol id="icon-user" viewBox="0 0 28 28"><title>user</title><path d="M14 22.422q1.859 0 3.91-1.094t3.090-2.68q-0.055-1.531-2.461-2.57t-4.539-1.039-4.539 1.012-2.461 2.598q1.039 1.586 3.090 2.68t3.91 1.094zM14 5.852q-1.422 0-2.461 1.039t-1.039 2.461 1.039 2.461 2.461 1.039 2.461-1.039 1.039-2.461-1.039-2.461-2.461-1.039zM14 2.352q4.813 0 8.23 3.418t3.418 8.23-3.418 8.23-8.23 3.418-8.23-3.418-3.418-8.23 3.418-8.23 8.23-3.418z"></path></symbol><symbol id="icon-home" viewBox="0 0 28 28"><title>home</title><path d="M11.648 23.352h-5.797v-9.352h-3.5l11.648-10.5 11.648 10.5h-3.5v9.352h-5.797v-7h-4.703v7z"></path></symbol><symbol id="icon-info" viewBox="0 0 28 28"><title>info</title><path d="M15.148 10.5v-2.352h-2.297v2.352h2.297zM15.148 19.852v-7h-2.297v7h2.297zM14 2.352q4.813 0 8.23 3.418t3.418 8.23-3.418 8.23-8.23 3.418-8.23-3.418-3.418-8.23 3.418-8.23 8.23-3.418z"></path></symbol><symbol id="icon-start" viewBox="0 0 28 28"><title>start</title><path d="M19.086 16.352h3.938q0.328-1.531 0.328-2.352t-0.328-2.352h-3.938q0.164 1.148 0.164 2.352t-0.164 2.352zM17.008 22.805q1.367-0.438 2.844-1.668t2.242-2.488h-3.445q-0.547 2.188-1.641 4.156zM16.734 16.352q0.164-1.148 0.164-2.352t-0.164-2.352h-5.469q-0.164 1.148-0.164 2.352t0.164 2.352h5.469zM14 23.297q1.531-2.242 2.242-4.648h-4.484q0.711 2.406 2.242 4.648zM9.352 9.352q0.656-2.352 1.641-4.156-1.367 0.438-2.871 1.668t-2.215 2.488h3.445zM5.906 18.648q0.711 1.258 2.215 2.488t2.871 1.668q-1.094-1.969-1.641-4.156h-3.445zM4.977 16.352h3.938q-0.164-1.148-0.164-2.352t0.164-2.352h-3.938q-0.328 1.531-0.328 2.352t0.328 2.352zM14 4.703q-1.531 2.242-2.242 4.648h4.484q-0.711-2.406-2.242-4.648zM22.094 9.352q-0.766-1.258-2.242-2.488t-2.844-1.668q0.984 1.805 1.641 4.156h3.445zM14 2.352q4.813 0 8.23 3.418t3.418 8.23-3.418 8.23-8.23 3.418-8.23-3.418-3.418-8.23 3.418-8.23 8.23-3.418z"></path></symbol></defs></svg>

<header class="w-full">
  <nav class="flex items-center h-16">
    {#if currentPage === "/"}
      <button on:click={toggle}>
        <Icon {size} name={open ? "close" : "menu"} />
      </button>
    {:else}
      <button on:click={() => history.back()}>
        <Icon {size} name="left" />
      </button>
    {/if}

    <div class="flex-grow text-2xl h-16 flex items-center px-2">{name}</div>

    {#if currentPage === "/"}
      {#if !$user}
        <button>
          <Icon {size} name="start" />
        </button>
      {:else}
        <button>
          <Icon {size} name="user" />
        </button>
      {/if}
    {:else}
      <button on:click={toggle}>
        <Icon {size} name={open ? "close" : "more"} />
      </button>
    {/if}
  </nav>
</header>

<style>
  header {
    --app-bar-color: #e0e0e0;
    --app-bar-bg: #2172d2;
    --app-bar-border: 1px solid #dddddd;
    --app-bar-item-h: 56px;
    --app-bar-item-w: 48px;
    background-color: var(--app-bar-bg);
    color: var(--app-bar-color);s
  }
  button {
    @apply inline-flex items-center justify-center text-center min-h-16 min-w-16 cursor-pointers hover:opacity-90 focus:outline-none;
  }
</style>
