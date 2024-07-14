<script lang="ts">
	import { base } from '$app/paths';
	import { page } from '$app/stores';

	$: pathname = $page.url.pathname;
</script>

<!-- <nav>
	<a href="{base}/" class:active={pathname === `${base}/`}>home</a>
	<a href="{base}/shop" class:active={pathname === `${base}/shop`}>shop</a>
</nav> -->

<slot />

<style>
</style>
