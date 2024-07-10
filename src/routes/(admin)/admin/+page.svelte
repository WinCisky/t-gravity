<script lang="ts">
	import PocketBase, { type ListResult, type RecordModel } from 'pocketbase';
	import { goto } from '$app/navigation';
	import { base } from '$app/paths';
	import { onMount } from 'svelte';

	const pb = new PocketBase('https://dev.opentrust.it/');

	let payments: ListResult<RecordModel> | null = null;

	async function getPayments(page = 1) {
		payments = await pb.collection('t_gravity_payments').getList(1, 20, {
			filter: 'completed = true',
			sort: '-created'
		});
		console.log(payments);
	}

	function formatDate(timestamp: string) {
		return new Date(timestamp).toLocaleDateString('en-US', {
			year: 'numeric',
			month: 'long',
			day: 'numeric',
			hour: '2-digit',
			minute: '2-digit'
		});
	}

	onMount(async () => {
		getPayments();
	});
</script>

<div class="container mx-auto my-10">
	<div class="divide-y divide-gray-200 overflow-hidden rounded-lg bg-white shadow">
		<div class="px-4 py-5 sm:px-6">
			<div class="text-xl font-semibold leading-6 text-gray-900">Payments</div>
		</div>
		<div class="px-4 py-5 sm:p-6">
			<div class="px-4 sm:px-6 lg:px-8">
				<div class="mt-8 flow-root">
					<div class="-mx-4 -my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
						<div class="inline-block min-w-full py-2 align-middle sm:px-6 lg:px-8">
							<table class="min-w-full divide-y divide-gray-300">
								<thead>
									<tr>
										<th
											scope="col"
											class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">Date</th
										>
										<th
											scope="col"
											class="py-3.5 pl-4 pr-3 text-left text-sm font-semibold text-gray-900 sm:pl-0"
											>Name</th
										>
										<th
											scope="col"
											class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">Email</th
										>
										<th
											scope="col"
											class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">Amount</th
										>
										<th scope="col" class="relative py-3.5 pl-3 pr-4 sm:pr-0">
											<span class="sr-only">View</span>
										</th>
									</tr>
								</thead>
								<tbody class="divide-y divide-gray-200">
									{#if payments}
										{#each payments?.items as payment}
											<tr>
												<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500"
													>{formatDate(payment.created)}</td
												>
												<td
													class="whitespace-nowrap py-4 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-0"
													>{payment.capture.payer.name.given_name}</td
												>
												<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500"
													>{payment.capture.payer.email_address}</td
												>
												<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500"
													>{payment.amount}</td
												>
												<td
													class="relative whitespace-nowrap py-4 pl-3 pr-4 text-right text-sm font-medium sm:pr-0"
												>
													<a href="{base}/admin/order?id={payment.id}" class="text-indigo-600 hover:text-indigo-900"
														>View<span class="sr-only"></span></a
													>
												</td>
											</tr>
										{/each}
									{/if}

									<!-- More people... -->
								</tbody>
							</table>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
