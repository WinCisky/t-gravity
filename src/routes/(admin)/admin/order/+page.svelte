<script lang="ts">
	import PocketBase, { type ListResult, type RecordModel } from 'pocketbase';
	import { onMount } from 'svelte';

	const pb = new PocketBase('https://dev.opentrust.it/');
    let order: ListResult<RecordModel> | null = null;

    onMount(async () => {
        const urlParams = new URLSearchParams(window.location.search);
        const id = urlParams.get('id');
        if (id) {
            order = await pb.collection('t_gravity_payments').getOne(id);
        }
    });
</script>

<h1>{JSON.stringify(order)}</h1>