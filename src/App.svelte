<script>
	// export let name;
	// export let age;
	import ContactCard from './ContactCard.svelte';
	
	let name = 'Roig';
	let age = 29

	// let uppercaseName; not required;

	$: uppercaseName = name.toUpperCase();
		// labeled statment and dynamic recalculation
	
	$: console.log(name);

	$: if (name === 'Roig') {
		console.log('it runs!');
		age = 29;
	}


	
	function incrementAge() {
		age += 1;
	}

	function changeName() {
		name = 'Roigus';


	}

	function nameInput(event){

		const enteredValue = event.target.value;
		name = enteredValue;


	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {uppercaseName}, my age is {age}!</h1>
<!-- <h1>Hello {name.UpperCase}, my age is {age}!</h1> also optional-->
<button on:click="{incrementAge}">Change age</button>
<button on:click="{changeName}">Change Name</button>

<!-- Quotation marks are not required above, they are for helping to highlight syntax. -->

<!-- <input type="text" value="{name}"on:input={nameInput} /> -->

<input type="text" bind:value={name} />

<!-- Short cut from the longer form above convenient for form and text input. Can theoretically bind any if most HTML props
don't overuse  -->
<ContactCard />