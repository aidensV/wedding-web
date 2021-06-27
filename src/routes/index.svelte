<script context="module">
	export const prerender = true;
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<div class="container">
		<img src="1.svg" alt="Snow" style="width:100%" />
		<a sveltekit:prefetch href="/index2" class="btn">Next</a>
	</div>
</section>

<style>
	.container {
		position: relative;
		width: 100%;
		max-width: 720px;
	}
	.container .btn {
		position: absolute;
		top: 50%;
		left: 95%;
		transform: translate(-50%, -50%);
		-ms-transform: translate(-50%, -50%);
		background-color: #555;
		color: white;
		font-size: 16px;
		padding: 12px 24px;
		border: none;
		cursor: pointer;
		border-radius: 5px;
		text-align: center;
		box-shadow: 0 9px 18px 0 #333333, 0 8px 24px 0 #333333;
	}
	

	.container .btn:hover {
		background-color: black;
	}
</style>
