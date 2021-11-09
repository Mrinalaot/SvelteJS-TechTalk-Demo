<script>
  import { afterUpdate, beforeUpdate, onDestroy, onMount } from "svelte";

  let posts = [];

  onMount(async () => {
    console.log("Component Mounted")
    setTimeout(async () => {
      const res = await fetch(`https://jsonplaceholder.typicode.com/posts`);
      posts = await res.json();
      console.log(posts);
    }, 5000);

  });

  beforeUpdate(() => {
    console.log('beforeUpdate')
  })
  afterUpdate(() => {
    console.log('afterUpdate')
  })

  onDestroy(() => {
    console.log("Component Destroyed");
  });

</script>

<div>
  {#each posts as post}
    {#if post.userId == 1}
      <h1>Name : {post.title}</h1>
      <h2>Age: {post.body}</h2>
    {:else}
      <h1>Not from userId 1</h1>
    {/if}
  {:else}
    <h1>Loading Posts ...</h1>
  {/each}
</div>
