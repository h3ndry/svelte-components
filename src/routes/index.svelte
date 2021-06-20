<script context="module">
	import { browser, dev } from '$app/env';
	import SuscribePopUp from '$lib/SuscribePopUp/index.svelte';

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
	<title>About</title>
</svelte:head>

<div class="container">
	<span class="oval oval-big" />
	<span class="oval oval-small" />
	<SuscribePopUp />
</div>

<style>
	.container {
		position: relative;
        min-height: 72vh;
        /* background-color: red; */
        display: grid;
        align-content: center;
	}

	.oval {
		border-radius: 50%;
		position: absolute;
		display: block;
		z-index: -1;
		filter: blur(1rem);
	}

	.oval.oval-small {
		height: 12rem;
		width: 12rem;
		background: linear-gradient(90deg, #ffd7ae, #ffb3af);
        transform: translate(-50%,-50%);
        top: 65%;
        left: 30%;
	}

	.oval.oval-big {
		background: linear-gradient(45deg, #aadbff, #ffb3af);
        top: 40%;
        left: 60%;
		height: 16rem;
        transform: translate(-50%,-50%);
		width: 16rem;
	}
</style>
