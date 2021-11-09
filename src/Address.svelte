<script>
    export let firstName = '';
    export let lastName = '';
    export let town = '';

    $: fullName = `${firstName} ${lastName}`;
    $: console.log('Name change Detedted',fullName)
</script>

<input type="text" bind:value={firstName}>
<input type="text" bind:value={lastName}>
<input type="text" bind:value={town}>

<h1> User - {fullName}</h1>
<h2> Address - {town} </h2>
