<script>
	// export let name;
	// export let age;
	let name = 'Roig';
	let age = 29

	function incrementAge() {
		age += 1;
	}

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name}, my age is {age}!</h1>

<button on:click="{incrementAge}">Change age</button>

<!-- Quotation marks are not required above, they are for helping to highlight syntax. -->