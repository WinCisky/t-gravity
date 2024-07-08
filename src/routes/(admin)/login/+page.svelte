<script lang="ts">
	import PocketBase from 'pocketbase';
	import { goto } from '$app/navigation';
	import { base } from '$app/paths';

	const pb = new PocketBase('https://dev.opentrust.it/');

	async function isAdmin() {
		const userId = pb.authStore.model?.id;
		const admins = await pb.collection('t_gravity_admins').getList(1, 1, {
			filter: `user.id = "${userId}"`
		});
		return admins.totalItems > 0;
	}

	async function login() {
		const authData  = await pb.collection('users').authWithOAuth2({ provider: 'google' });
		if (pb.authStore.isValid && await isAdmin()) {
			goto(`${base}/admin`);
		}
	}
</script>

<svelte:head>
	<title>Admin</title>
	<!-- noindex -->
	<meta name="robots" content="noindex" />
</svelte:head>

<h1>Login</h1>

<button on:click={login}>Login with Google</button>