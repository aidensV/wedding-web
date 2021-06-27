<script context="module">
	import { browser, dev } from '$app/env';

// we don't need any JS on this page, though we'll load
// it in dev so that we get hot module replacement...
export const hydrate = dev;

// ...but if the client-side router is already loaded
// (i.e. we came here from elsewhere in the app), use it
export const router = browser;

// since there's no dynamic data here, we can prerender
// it so that it gets served as a static asset in prod
export const prerender = true;
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<div class="container">
		<img src="2.svg" alt="Snow" style="width:100%" />
		<a sveltekit:prefetch href="/" class="btn">Prev</a>
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
		left: 5%;
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
