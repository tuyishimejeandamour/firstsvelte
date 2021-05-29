<script>
 let name ="dobby";
 let lastname="";
 let firstname="";

 //reactive variable we use dollar sign and name of that reactive varialble

 $: fullname =`${lastname} ${firstname}`;
 //some time you may use also reactive statement and it will check every time either of the variable change
 
 $: {
	 //this is to mean that if any of the first and lastname change the this code block will run
	 console.log(fullname);
	 console.log(name);
 }


</script>

<main>
	<p>{fullname}</p>
	<input type="text" bind:value={firstname}>
	<input type="text" bind:value={lastname}>
</main>


<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>