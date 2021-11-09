<script>
	import Library from './Library.svelte';
	import Address from './Address.svelte';
	import Post from './Post.svelte';
	// let library = 'React';
	// const switchLibrary = () => {
	// 	library = library === 'React' ? 'Svelte' : 'React';
	// }
	const LibraryInfo = {
		name: 'Angular',
		version: 9.0,
		isMajor: false,
	}
</script>

<main>
	<!-- <h1> My Favourite Library - {library} </h1>
	<button on:click={switchLibrary}> Switch </button> -->
	<Library name={'React'} version={16.8} isMajor={true}/>
	<Library></Library>
	<Library {...LibraryInfo}></Library>
	<hr>
	<Address/>
	<hr>
	<Post/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}
	/* h1 {
		color:blue;
	} */
</style>