<script lang="ts">
	import PocketBase, { type ListResult, type RecordModel } from 'pocketbase';
	import { onMount } from 'svelte';

	const pb = new PocketBase('https://dev.opentrust.it/');
    export let data;
    let order: ListResult<RecordModel> | null = null;

    onMount(async () => {
        order = await pb.collection('t_gravity_payments').getOne(data.id);
    });
</script>

<h1>{JSON.stringify(order)}</h1>