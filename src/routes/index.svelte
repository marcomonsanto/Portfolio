<script lang="typescript">
  import Button from '../components/Button.svelte';
  export let title: string = "Hello sapper typescript";
</script>

<svelte:head>
  <title>{title}</title>
</svelte:head>

<div class="flex sm:flex-row flex-col py-20">
	<div class="flex flex-col justify-center w-full sm:w-1/2 sm:mb-0 mb-20">
		<h1 class="text-4xl md:text-6xl mb-6">Marco Monsanto</h1>
		<p class="text-lg mb-12">Software Developer helping clients implemented their vision in web apps.</p>
		<Button on:click={() => console.log('what')}>Message me!</Button>
	</div>
  <div class="flex flex-col justify-center w-full sm:w-1/2">
    <img
      class=""
      alt="Connection the businesses and customers"
      src="connection.svg" />
  </div>
</div>

<p>
  <strong>
    Try editing this file (src/routes/index.svelte) to test live reloading.
  </strong>
</p>
