<script>
  import AppBar from "$lib/components/AppBar.svelte";
</script>

<AppBar />



<slot />

<style windi:preflights:global windi:safelist:global global>
  :root {
    --app-body-color: #424656;
    --app-body-bg: #ffffff;
    --app-bar-color: #e0e0e0;
    --app-bar-bg: #2172d2;
    --app-bar-border: 1px solid #dddddd;
    --app-bar-item-h: 56px;
    --app-bar-item-w: 48px;
    --column-width: 680px;
    --column-margin-top: 1rem;
    --column-padding: 1rem;
  }
  :global(body) {
    @apply text-gray-600;
  }

  :global(#app) {
    @apply absolute inset-0 overflow-hidden flex flex-col;
  }

  h1,
  h2,
  h3,
  h4,
  h5 {
    @apply text-xl mt-0 mb-1 font-normal leading-normal;
  }

  .h1,
  .h2,
  .h3,
  .h4,
  .h5,
  .h6 {
    @apply text-xl mt-0 mb-0 font-normal leading-normal;
  }

  h1,
  .h1 {
    @apply text-6xl;
  }

  h2,
  .h2 {
    @apply text-5xl;
  }

  h3,
  .h3 {
    @apply text-4xl;
  }

  h4,
  .h4 {
    @apply text-3xl;
  }

  h5,
  .h5 {
    @apply text-2xl;
  }

  h6,
  .h6 {
    @apply text-xl;
  }

  p {
    @apply text-lg mb-1 text-blueGray-500 leading-relaxed;
  }

  pre {
    @apply p-2 bg-gray-50 overflow-x-auto text-gray-400;
  }

  .input {
    @apply block w-full px-6 py-2 font-light text-base border border-gray-300 rounded;
  }

  .checkbox {
    @apply h-8 w-8 rounded border-gray-300;
  }

  .nwp-button {
    @apply inline-block whitespace-nowrap px-6 py-2.5 text-base rounded leading-tight uppercase shadow-md hover: shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg transition duration-150 ease-in-out;
  }

  .nwp-button.red {
    @apply bg-red-600 text-white hover: bg-red-700 active:bg-red-800;
  }

  .nwp-button.blue {
    @apply bg-blue-600 text-white hover: bg-blue-700 active:bg-blue-800;
  }

  .nwp-button.light {
    @apply bg-gray-200 text-gray-700 hover: bg-gray-300 active:bg-gray-400;
  }

  .nwp-button.link {
    @apply bg-transparent text-blue-600;
  }
</style>
