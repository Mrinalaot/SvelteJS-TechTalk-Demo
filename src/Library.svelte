<script>
  export let name = "Svelte";
  export let version = 3.1;
  export let isMajor = false;
  let rating = 0;
//   const handleInput = (e) => {
//       rating = e.target.value;
//   };
</script>

<h1>Name : {name}</h1>
<!-- <h2 class={isMajor ? 'major': '' }>Version: {version} !</h2> -->
<h2 class:major={isMajor}>Version: {version} !</h2>

<!-- <input type="text" on:input={handleInput} value={rating}/> -->
<input type="text" bind:value={rating}/>
<button on:click={()=> rating = 10}>Give full rating</button>
<h3>Rating - {rating}</h3>

<style>
  h1 {
    color: blue;
  }
  .major {
    color: red;
    font-style: italic;
  }
</style>
