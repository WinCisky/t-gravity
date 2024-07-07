<script lang="ts">
	import { base } from '$app/paths';
	import magOneImg1 from '$lib/images/t-mag/image1.png';
</script>

<svelte:head>
	<title>T-Gravity</title>
	<meta name="description" content="t-gravity shop" />
</svelte:head>

<h1>Shop</h1>

<div>
	<a href="{base}/shop/t-mag">
		<img src={magOneImg1} alt="immagine t-mag" />
		<p>T-Mag</p>
	</a>
</div>
