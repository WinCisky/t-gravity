<script lang="ts">
	import { page } from '$app/stores';

	$: pathname = $page.url.pathname;
</script>

<nav>
	<a href="/" class:active={pathname === '/'}>home</a>
	<a href="/shop" class:active={pathname === '/shop'}>shop</a>
	<a href="/about" class:active={pathname === '/about'}>about</a>
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
