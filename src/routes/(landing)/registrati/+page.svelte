<script lang="ts">
	import { onMount } from 'svelte';
	let email: string = '';

    const RECAPTCHA_SITE_KEY = '6LdsDAYqAAAAADEep-i5jbfTZ7BF_HMXGrYUnf8Z';
	let error: string = '';
	let info: string = '';
	let timeout: number;

	onMount(() => {
		// Load the reCAPTCHA script
		const script = document.createElement('script');
		script.src = 'https://www.google.com/recaptcha/api.js?render=' + RECAPTCHA_SITE_KEY;
		document.body.appendChild(script);
	});

	function showErrorMessage(msg?: string) {
		error = `Error registering user: ${msg || 'Please try again'}`;
		timeout = setTimeout(() => {
			error = '';
		}, 5000);
	}

	function showInfoMessage() {
		info = 'User registered successfully';
		timeout = setTimeout(() => {
			info = '';
		}, 5000);
	}

	async function registerUser() {
        console.log('registering user');
        // @ts-ignore
		grecaptcha.ready(function () {
            console.log('grecaptcha ready');
            // @ts-ignore
			grecaptcha.execute(RECAPTCHA_SITE_KEY, { action: 'submit' }).then(async function (
				token: string
			) {
				const response = await fetch('https://t-gravity.deno.dev/register-email', {
					method: 'POST',
					headers: {
						'Content-Type': 'application/json'
					},
					body: JSON.stringify({ email, recaptchaToken: token })
				});

				clearTimeout(timeout);

				if (!response.ok) {
					showErrorMessage();
					return;
				}

				const data = await response.json();
				if (data.error) {
					showErrorMessage(data.error);
					return;
				}

				// Handle success
				showInfoMessage();
			});
		});
	}
</script>

<main>
	<h1>Registrati</h1>
	<form on:submit|preventDefault={registerUser}>
		<div>
			<label for="email">Email:</label>
			<input id="email" type="email" bind:value={email} required />
		</div>
		<button type="submit">Register</button>
	</form>
	{#if error}
		<p style="color: red">{error}</p>
	{/if}
	{#if info}
		<p style="color: green">{info}</p>
	{/if}
</main>
