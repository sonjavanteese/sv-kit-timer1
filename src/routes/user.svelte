<script>
  import Header from '$lib/components/Header.svelte';
  import {user} from '$lib/stores';
  import {pages} from '$lib/db';
  let pD = pages[2];
</script>

<main class="page">
  <Header {...pD} />
  <article class="container mx-auto px-4 py-4 space-y-8">
    {#if $user}
      User
    {/if}
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis impedit
      similique, vel quas molestias dolorem blanditiis sit? Eum non reiciendis
      voluptate fuga tenetur est quis! Praesentium consequatur labore explicabo
      pariatur.
    </p>
    <div>
      <ul>
        {#each pages as {name, path}}
        <li>
          <a href={path}>{name}</a>
        </li>
        {/each}
      </ul>
    </div>

  </article>
</main>

<style global>
  .page {
    @apply flex-grow overflow-y-auto;
  }

</style>
