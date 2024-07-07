<script lang="ts">
    import { type Propriety } from '$lib/types';
	import { onMount } from 'svelte';
	import { loadScript } from '@paypal/paypal-js';
    import Swiper from 'swiper';
    import 'swiper/css';

	const clientId = "Aa8zMMxnb1NiwTIbw64BhpgP53K87uw7R3kRqVtSaGkuEgiuY8Qz3oEP2V3A1UQc3rDVrZyD5mATNZsK";
    const backendUrl = "https://t-gravity.deno.dev";

	export let productId;
	export let variants: Propriety[] = [];
	export let proprieties: Propriety[] = [];

	let selectedVariant = variants[0];
	let selectedProprieties = new Map<string, string>();

	proprieties.forEach((propriety) => {
		selectedProprieties.set(propriety.name, propriety.values[0].value);
	});

	onMount(async () => {

        const swiper = new Swiper('.swiper', {
            // Optional parameters
            direction: 'horizontal',
            loop: true,

            // If we need pagination
            pagination: {
                el: '.swiper-pagination',
            },

            // Navigation arrows
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },

            // And if we need scrollbar
            scrollbar: {
                el: '.swiper-scrollbar',
            },
        });

		let paypal;

		try {
			paypal = await loadScript({
				clientId: clientId,
				currency: 'EUR'
			});
		} catch (error) {
			console.error('failed to load the PayPal JS SDK script', error);
		}

		if (paypal) {
			try {
				// @ts-ignore
				await paypal
					.Buttons({
						async createOrder() {
							try {
								const response = await fetch(`${backendUrl}/create-paypal-order`, {
									method: 'POST',
									headers: { 'Content-Type': 'application/json' },
									body: JSON.stringify({
										amount: "100.00",
										cart: [{ id: productId, proprieties: Object.fromEntries(selectedProprieties.entries()) }]
									})
								});

								const orderData = await response.json();
								console.log(orderData);

								if (!orderData.id) {
									const errorDetail = orderData.details[0];
									const errorMessage = errorDetail
										? `${errorDetail.issue} ${errorDetail.description} (${orderData.debug_id})`
										: 'Unexpected error occurred, please try again.';

									throw new Error(errorMessage);
								}

								return orderData.id;
							} catch (error) {
								console.error(error);
								throw error;
							}
						}
					})
					.render('#paypal-button');
			} catch (error) {
				console.error('failed to render the PayPal Buttons', error);
			}
		}
	});
</script>

<div>
	<div>
		<!-- Slider main container -->
		<div class="swiper">
			<!-- Additional required wrapper -->
			<div class="swiper-wrapper">
				<!-- Slides -->
                {#each selectedVariant.values as variant}
                    <div class="swiper-slide">
                        <img src={variant.value} alt={variant.name} />
                    </div>
                {/each}
			</div>
			<!-- If we need pagination -->
			<div class="swiper-pagination"></div>

			<!-- If we need navigation buttons -->
			<div class="swiper-button-prev"></div>
			<div class="swiper-button-next"></div>

			<!-- If we need scrollbar -->
			<div class="swiper-scrollbar"></div>
		</div>
		<p>T-Mag</p>
	</div>
	<div>
        {#if variants.length > 1}
		<div>
            <fieldset>
                <legend>Variant</legend>
                {#each variants as variant, i}
                    <div>
                        <input
                            type="radio"
                            id={variant.name}
                            name={variant.name}
                            value={variant.name}
                            checked={i === 0}
                            on:change={() => selectedVariant = variant}
                        />
                        <label for={variant.name}>{variant.name}</label>
                    </div>
                {/each}
            </fieldset>
		</div>
        {/if}
		<div>
			{#each proprieties as propriety}
				<fieldset>
					<legend>{propriety.name}</legend>
					{#each propriety.values as prop, i}
						<div>
							<input
								type="radio"
								id={prop.name}
								name={propriety.name}
								value={prop.name}
								checked={i === 0}
								on:change={() => selectedProprieties.set(propriety.name, prop.value)}
							/>
							<label for={prop.name}>{prop.name}</label>
						</div>
					{/each}
				</fieldset>
			{/each}
		</div>
	</div>
</div>
<div>
	<div id="paypal-button"></div>
</div>
