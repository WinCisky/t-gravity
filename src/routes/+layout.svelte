<script lang="ts">
	import { base } from '$app/paths';
	import { page } from '$app/stores';

	$: pathname = $page.url.pathname;
</script>

<nav>
	<a href="{base}/" class:active={pathname === `${base}/`}>home</a>
	<a href="{base}/shop" class:active={pathname === `${base}/shop`}>shop</a>
	<a href="{base}/about" class:active={pathname === `${base}/about`}>about</a>
</nav>

<slot />

<style>
	nav {
		display: flex;
	}
	nav a {
		margin-right: 10px;
	}
	nav a.active {
		font-weight: bold;
	}
</style>
