<script lang="ts">
    import { type Propriety } from '$lib/types';

	import magOneImg1 from '$lib/images/t-mag/image1.png';
	import magOneImg2 from '$lib/images/t-mag/image2.png';
	import Product from '../../../components/product.svelte';

	const productId = 1;
	const variants: Propriety[] = [
		{
			name: 'one',
			values: [
				{
					name: 'mag one img 1',
					value: magOneImg1
				},
				{
					name: 'mag one img 2',
					value: magOneImg2
				},
			]
		},
	];
	const proprieties: Propriety[] = [
		{
			name: 'size',
			values: [
				{
					name: 'small',
					value: 's'
				},
				{
					name: 'medium',
					value: 'm'
				},
				{
					name: 'large',
					value: 'l'
				},
				{
					name: 'extra large',
					value: 'xl'
				}
			]
		}
	];


</script>

<svelte:head>
	<title>T-Gravity</title>
	<meta name="description" content="t-gravity shop" />
</svelte:head>

<h1>T-Mag</h1>
<Product {productId} {variants} {proprieties} />
<p>
	Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras pellentesque mauris arcu, ut blandit
</p>
