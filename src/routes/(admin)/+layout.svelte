<script lang="ts">
	import { base } from '$app/paths';
	import { page } from '$app/stores';
    import PocketBase from 'pocketbase';
    import { goto } from '$app/navigation';
    import { onMount } from 'svelte';
    
	$: pathname = $page.url.pathname;
    
    const pb = new PocketBase('https://dev.opentrust.it/');

    onMount(async () => {
        if (
            !pb.authStore.isValid &&
            pathname !== `${base}/login`
        ) {
            goto(`${base}/login`);
        }
    });
</script>

<slot />