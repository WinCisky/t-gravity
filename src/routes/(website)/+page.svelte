<script lang="ts">
	import { base } from '$app/paths';

	import logo from '$lib/images/home/logo.webp';
	import logoAureo from '$lib/images/home/logo_aureo.webp';
	import photoShirt from '$lib/images/home/photo_shirt.webp';
	import beforeAfter from '$lib/images/home/prima-dopo-300x300.webp';
</script>

<svelte:head>
	<title>T-Gravity</title>
	<meta name="description" content="t-gravity" />
</svelte:head>

<div class="bg-white">
	<header class="absolute inset-x-0 top-0 z-50">
		<nav
			class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8"
			aria-label="Global"
		>
			<div class="flex lg:flex-1">
				<a href="{base}/" class="-m-1.5 p-1.5">
					<span class="sr-only">T-Gravity</span>
					<img class="h-14 w-auto" src={logoAureo} alt="" />
				</a>
			</div>
			<div class="flex">
				<a href="{base}/shop/t-mag" class="text-xl font-semibold leading-6 text-gray-900">T-Mag</a>
			</div>
		</nav>
	</header>
	<div class="relative isolate overflow-hidden bg-gradient-to-b from-sky-100/20 pt-14">
		<div
			class="absolute inset-y-0 right-1/2 -z-10 -mr-96 w-[200%] origin-top-right skew-x-[-30deg] bg-white shadow-xl shadow-sky-600/10 ring-1 ring-sky-50 sm:-mr-80 lg:-mr-96"
			aria-hidden="true"
		></div>
		<div class="mx-auto max-w-7xl px-6 py-32 sm:py-40 lg:px-8">
			<div
				class="mx-auto max-w-2xl lg:mx-0 lg:grid lg:max-w-none lg:grid-cols-2 lg:gap-x-16 lg:gap-y-6 xl:grid-cols-1 xl:grid-rows-1 xl:gap-x-8"
			>
				<h1
					class="max-w-2xl text-2xl font-bold tracking-tight text-gray-900 sm:text-4xl lg:col-span-2 xl:col-auto"
				>
					“La legge di gravitazione universale è una legge fisica fondamentale che afferma che
					nell’Universo due corpi si attraggono con una forza direttamente proporzionale”
				</h1>
				<div class="mt-6 max-w-xl lg:mt-0 xl:col-end-1 xl:row-start-1">
					<div class="font-semibold text-gray-900">Newton/Hooke</div>
				</div>
				<img
					src={logo}
					alt="logo t-gravity"
					class="mt-10 aspect-[6/5] w-full max-w-lg rounded-2xl object-contain sm:mt-16 lg:mt-0 lg:max-w-none xl:row-span-2 xl:row-end-2 xl:mt-36"
				/>
			</div>
		</div>
		<div class="absolute inset-x-0 bottom-0 -z-10 h-24 bg-gradient-to-t from-white sm:h-32"></div>
	</div>
</div>

<div class="bg-white py-24 sm:py-32">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-none">
			<!-- <p class="text-base font-semibold leading-7 text-sky-600">Deploy faster</p>
			<h1 class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
				A better workflow
			</h1> -->
			<div
				class="mt-10 grid max-w-xl grid-cols-1 gap-8 lg:max-w-none lg:grid-cols-2 text-xl text-gray-900 leading-8 sm:text-lg"
			>
				<div>
					<p>
						Il termine “gravità” deriva dall’aggettivo latino gravis, pesante. La parola viene
						generalmente ricondotta a situazioni complesse, pesanti appunto, nella vita di tutti i
						giorni: lavoro, cibo, stress etc. Ci ricorda molte delle azioni che facciamo
						quotidianamente in ogni momento della giornata.
					</p>
					<p class="mt-8">
						In realtà, ogni individuo è una massa fisica specifica che esercita una propria forza di
						gravità. Di conseguenza, molti disturbi e patologie sono causati dal fatto che la parte
						superiore del nostro corpo aiuta quella inferiore proprio nella lotta contro la gravità.
					</p>
				</div>
				<div>
					<p>
						Un comune mal di schiena, ad esempio, segnala questo limite, come una spia che si
						accende quando l’usura dei tessuti è eccessiva. Il problema è il conflitto tra muscoli
						agonisti e muscoli antagonisti. Se i muscoli antagonisti sono contratti per permettermi
						di vincere la forza di gravità, il muscolo agonista entra in conflitto e, ogni volta che
						si contrae, trova l’ostacolo del muscolo antagonista. Questi attriti sono quelli che poi
						usurano il corpo, a livello articolare, ma anche a livello dell’endotelio dei condotti
						in cui scorrono i fluidi, che vengono così rallentati.
					</p>
					<p class="mt-8">
						La tecnica T-Gravity migliora la tua flessibilità del corpo che è una caratteristica
						importante per la tua forma fisica e per la vita quotidiana di tutti i giorni.
					</p>
				</div>
			</div>
		</div>
	</div>
</div>

<section class="px-6 py-24 sm:py-32 lg:px-8">
	<figure class="relative mx-auto max-w-7xl">
		<svg
			viewBox="0 0 162 128"
			fill="none"
			aria-hidden="true"
			class="absolute -top-12 left-0 -z-10 h-32 stroke-gray-900/10"
		>
			<path
				id="b56e9dab-6ccb-4d32-ad02-6b4bb5d9bbeb"
				d="M65.5697 118.507L65.8918 118.89C68.9503 116.314 71.367 113.253 73.1386 109.71C74.9162 106.155 75.8027 102.28 75.8027 98.0919C75.8027 94.237 75.16 90.6155 73.8708 87.2314C72.5851 83.8565 70.8137 80.9533 68.553 78.5292C66.4529 76.1079 63.9476 74.2482 61.0407 72.9536C58.2795 71.4949 55.276 70.767 52.0386 70.767C48.9935 70.767 46.4686 71.1668 44.4872 71.9924L44.4799 71.9955L44.4726 71.9988C42.7101 72.7999 41.1035 73.6831 39.6544 74.6492C38.2407 75.5916 36.8279 76.455 35.4159 77.2394L35.4047 77.2457L35.3938 77.2525C34.2318 77.9787 32.6713 78.3634 30.6736 78.3634C29.0405 78.3634 27.5131 77.2868 26.1274 74.8257C24.7483 72.2185 24.0519 69.2166 24.0519 65.8071C24.0519 60.0311 25.3782 54.4081 28.0373 48.9335C30.703 43.4454 34.3114 38.345 38.8667 33.6325C43.5812 28.761 49.0045 24.5159 55.1389 20.8979C60.1667 18.0071 65.4966 15.6179 71.1291 13.7305C73.8626 12.8145 75.8027 10.2968 75.8027 7.38572C75.8027 3.6497 72.6341 0.62247 68.8814 1.1527C61.1635 2.2432 53.7398 4.41426 46.6119 7.66522C37.5369 11.6459 29.5729 17.0612 22.7236 23.9105C16.0322 30.6019 10.618 38.4859 6.47981 47.558L6.47976 47.558L6.47682 47.5647C2.4901 56.6544 0.5 66.6148 0.5 77.4391C0.5 84.2996 1.61702 90.7679 3.85425 96.8404L3.8558 96.8445C6.08991 102.749 9.12394 108.02 12.959 112.654L12.959 112.654L12.9646 112.661C16.8027 117.138 21.2829 120.739 26.4034 123.459L26.4033 123.459L26.4144 123.465C31.5505 126.033 37.0873 127.316 43.0178 127.316C47.5035 127.316 51.6783 126.595 55.5376 125.148L55.5376 125.148L55.5477 125.144C59.5516 123.542 63.0052 121.456 65.9019 118.881L65.5697 118.507Z"
			/>
			<use href="#b56e9dab-6ccb-4d32-ad02-6b4bb5d9bbeb" x="86" />
		</svg>
		<blockquote
			class="mt-10 text-xl leading-8 tracking-tight text-gray-900 sm:text-lg sm:leading-9"
		>
			<p>
				Eccomi qua, con un po’ di ritardo ma ci tenevo a scrivere questo messaggio in tranquillità e
				la mattina presto è l’unico momento in cui a casa c’è silenzio ed è il mio momento, in
				particolare dopo due giorni di fuoco con le bambine a casa da scuola, da riorganizzare la
				routine quotidiana ed ero da sola in istituto.
			</p>
			<br />
			<p>
				Ad ogni modo ti devo davvero ringraziare, sto veramente bene, la schiena non mi fa più male,
				nemmeno a letto che la mattina ero a pezzi, percepisco la sensazione di stare più dritta e
				più in equilibrio, non solo esternamente (fisicamente) ma anche proprio con me stessa.
				Nonostante queste ultime due giornate intense nel dovrer organizzare famiglia e lavoro
				(perché da parte del marito non ho molti aiuti) questa volta non sono andata in ansia come
				al solito solitamente somatizzo a livello di stomaco percependo in questi casi sempre una
				morsa che è lì che stringe ma questa volta ho affrontato tutto con più serenità e dal
				momento che solitamente non sono così ho pensato fosse merito del trattamento. Mi hai detto
				che avrei potuto dormire meglio ed è vero, molti meno risvegli, quelli purtroppo sono
				dettati anche dalla figlia che ancora ogni tanto si sveglia, ma quando dorme tutta la notte
				io dormo davvero bene. Da martedì percepisco una forte carica addosso, se prima ero sempre
				stanca ora andrei a correre tutte le mattine alle 6! Scherzi a parte sento molta più
				energia.
			</p>
			<br />
			<p>
				Un’ultima cosa e credo di poter collegare al trattamento anche questa, sono circa tre
				settimane che mi ero messa un po’ a regime alimentare nuovamente perché dopo il matrimonio
				di mia sorella, e le ferie, mi sono lasciata un po’ andare, non che mangi male ma magari
				intanto che preparo il pranzo/cena stuzzico, formaggi, pane ecc ecc e in tre settimane non
				avevo visto alcun risultato, sarà sicuramente colpa del metabolismo che sta rallentando, ma
				io giuro che ci ho provato a togliere gli extra e non perdevo peso. Bene, dopo questa
				premessa e dopo il compleanno di papà e dunque ho ahimè mangiato (bis di dolce compreso)
				questa mattina mi sentivo diversa e mi sono pesata, sono a -1kg e 8 in 5 giorni! Con molta
				probabilità riequilibrando tutto a 360 gradi il trattamento ha fatto sì che sbloccasse quel
				meccanismo che non faceva più stare bene e stando bene fisicamente, vedendomi meglio, è
				aumentata la mia autostima e sono scesa di peso velocemente. Wow mi sembra persino
				impossibile ma sto davvero bene gazie!
			</p>
			<br />
			<div class="relative mx-auto max-w-2xl py-24 sm:py-32 lg:max-w-4xl">
				<figure class="grid grid-cols-1 items-center gap-x-6 gap-y-8 lg:gap-x-10">
					<div class="col-end-1 w-16 lg:row-span-4 lg:w-72">
						<img
							class="rounded-xl bg-sky-50 lg:rounded-3xl"
							loading="lazy"
							src={beforeAfter}
							alt=""
						/>
					</div>
					<p>
						Ps: tutti i giorni provo a mettermi in squat per vedere se davvero sono ancora capace di
						stare in equilibrio questa cosa mi ha sconvolta! Sappi che appena barcollo arrivooooo
						Grazie ancora di tutto.
					</p>
					<figcaption class="text-base lg:col-start-1 lg:row-start-3">
						<div class="font-semibold text-gray-900">Elisa (40 anni)</div>
						<div class="mt-1 text-gray-500">Pordenone</div>
					</figcaption>
				</figure>
			</div>
		</blockquote>
	</figure>
</section>

<div class="overflow-hidden rounded-lg bg-white shadow max-w-6xl m-auto">
	<div class="px-4 py-5 sm:p-6">
		<div class="grid w-full grid-cols-1 items-start gap-x-6 gap-y-8 sm:grid-cols-12 lg:gap-x-8">
			<div class="sm:col-span-4 lg:col-span-5">
				<div class="aspect-h-1 aspect-w-1 overflow-hidden rounded-lg bg-gray-100">
					<img
						src={photoShirt}
						alt="Back angled view with bag open and handles to the side."
						class="object-cover object-center"
					/>
				</div>
			</div>
			<div class="sm:col-span-8 lg:col-span-7">
				<h2 class="text-2xl font-bold text-gray-900 sm:pr-12">Maglietta T-Gravity</h2>

				<section aria-labelledby="information-heading" class="mt-3">
					<h3 id="information-heading" class="sr-only">Product information</h3>

					<div class="mt-6 text-xl text-gray-900 leading-8 sm:text-base">
						<h4 class="sr-only">Description</h4>

						<p>
							Abbiamo completamente dimenticato la dimensione invisibile della nostra esistenza che
							è la più importante, perché in essa risiede il nostro vero potere e il vero
							significato della nostra vita.
						</p>
						<p>
							La vera essenza consiste nel riportare la nostra attenzione sull’invisibile,
							sull’anima. La prima cosa da esaminare è la linea di comunicazione tra la nostra
							fisicità e la nostra anima che è rappresentata da campi di plasma, uno stato
							premateria dell’universo.
						</p>
						<br />
						<p>
							Quando operiamo con i campi plasmatici dell’universo stabiliamo una linea di
							comunicazione tra il plasma e lo stato della materia.
						</p>
						<br />
						<p>
							La maglietta T-Gravity porta con sè il frutto del più alto livello di conoscenza dei
							campi plasmatici dell’universo e ne rappresenta un mezzo per accedere ad essi.
						</p>
					</div>
				</section>

				<section aria-labelledby="options-heading" class="mt-6">
					<h3 id="options-heading" class="sr-only">Product options</h3>

					<div class="mt-6">
						<a
							href="{base}/shop/t-mag"
							type="submit"
							class="flex w-full items-center justify-center rounded-md border border-transparent bg-sky-600 px-8 py-3 text-base font-medium text-white hover:bg-sky-700 focus:outline-none focus:ring-2 focus:ring-sky-500 focus:ring-offset-2 focus:ring-offset-gray-50"
							>Acquista
							</a>
					</div>
				</section>
			</div>
		</div>
	</div>
</div>

<div class="relative isolate bg-white pb-32 pt-24 sm:pt-32 mt-12">
	<div
		class="absolute inset-x-0 top-1/2 -z-10 -translate-y-1/2 transform-gpu overflow-hidden opacity-30 blur-3xl"
		aria-hidden="true"
	>
		<div
			class="ml-[max(50%,38rem)] aspect-[1313/771] w-[82.0625rem] bg-gradient-to-tr from-sky-200 to-cyan-200"
			style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"
		></div>
	</div>
	<div
		class="absolute inset-x-0 top-0 -z-10 flex transform-gpu overflow-hidden pt-32 opacity-25 blur-3xl sm:pt-40 xl:justify-end"
		aria-hidden="true"
	>
		<div
			class="ml-[-22rem] aspect-[1313/771] w-[82.0625rem] flex-none origin-top-right rotate-[30deg] bg-gradient-to-tr from-sky-200 to-cyan-200 xl:ml-0 xl:mr-[calc(50%-12rem)]"
			style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"
		></div>
	</div>
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-xl text-center">
			<p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
				I nostri feedback
			</p>
		</div>
		<div
			class="mx-auto mt-16 grid max-w-2xl grid-cols-1 grid-rows-1 gap-8 text-sm leading-6 text-gray-900 sm:mt-20 sm:grid-cols-2 xl:mx-0 xl:max-w-none xl:grid-flow-col xl:grid-cols-4"
		>
			<figure
				class="col-span-2 hidden sm:block sm:rounded-2xl sm:bg-white sm:shadow-lg sm:ring-1 sm:ring-gray-900/5 xl:col-start-2 xl:row-end-1"
			>
				<blockquote class="p-12 text-xl font-semibold leading-8 tracking-tight text-gray-900">
					<p>
						La mia ragazzina disabile, con difficoltà ad esprimere emozioni o pensieri, non riusciva
						a gestire la rabbia, c’erano scatti improvvisi che la mettevano in pericolo o feriva chi
						le era vicino; da quando ha indossato la maglietta “magica” risponde a tono, c’è sempre
						il “boh” prima, ma poi si esprime in modo comprensibile e appropriato, decisamente più
						calma e cosa mai fatta, mi dice spesso “grazie mamma” come se avesse acquisito
						consapevolezza. Mi par di vivere un sogno!!
					</p>
				</blockquote>
				<figcaption class="flex items-center gap-x-4 border-t border-gray-900/10 px-6 py-4">
					<div class="flex-auto">
						<div class="font-semibold">Marianna</div>
						<div class="text-gray-600">Veneto</div>
					</div>
				</figcaption>
			</figure>
			<div class="space-y-8 xl:contents xl:space-y-0">
				<div class="space-y-8 xl:row-span-2">
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Ho indossato la maglietta T Gravity la prima notte e per circa un’ora ed ho fatto
								molti scatti di scarico tensione, la seconda notte meno e la terza non ho ricordo di
								altri scatti.
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Raffaello (61 anni)</div>
								<div class="text-gray-600">Sacile</div>
							</div>
						</figcaption>
					</figure>

					<!-- More testimonials... -->
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Buongiorno, ho provato la maglietta e devo dire che per due notti di seguito ho
								fatto dei sogni molto particolari ma uno sembrava proprio una costellazione
								familiare in pieno, perché c’erano avi, non miei del mio ex fidanzato, riguardava
								tutta una linea femminile.
							</p>
							<br />
							<p>
								Mi stavano dicendo davanti una tavolata, che dovevo seguire tutti gli schemi
								familiari per essere accettati in famiglia c’è proprio costellazioni in pieno e me
								lo sono ricordato tutto anche la notte dopo fatto un altro sogno che me lo sono
								ricordato tutto su Intuizioni seguire le proprie intuizioni e così e poi forse ho
								avuto dei sogni un po’ frammentati nel senso che non ho grandi ricordi poi 2 scene
								particolari.
							</p>
							<p>Grazie!</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Paola (53 anni)</div>
								<div class="text-gray-600">Pordenone</div>
							</div>
						</figcaption>
					</figure>

					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>Buongiorno,</p>
							<br />
							<p>Ecco il feedback dopo aver testato la maglietta per alcune notti.</p>
							<br />
							<p>
								Già l’atto di indossarla risulta piacevole al tatto, per il materiale stesso di cui
								è fatta la maglietta.
							</p>
							<br />
							<p>
								Nelle notti in cui l’ho indossata sotto al pigiama, mi è capitato di svegliarmi e
								constatare che la sveglia segnava ancora alcune ore a disposizione prima del
								risveglio e questa è sempre una piacevole sorpresa, perché normalmente mi capita
								esattamente l’opposto.
							</p>
							<br />
							<p>
								Ho quindi avvertito la sensazione di essere molto più riposato del normale, anche
								solo con poche ore di sonno, così le restanti a disposizione risultino più un
								“bonus” che non una vera e propria necessità.
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Michele (38 anni)</div>
								<div class="text-gray-600">Ferrara</div>
							</div>
						</figcaption>
					</figure>

					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Buonasera a tutti , condivido la mia personale esperienza che ho avuto indossando la
								t-shirt T-Gravity Diventata asmatica da circa 10 anni a causa di un virus da aria
								condizionata/pressorizzata aereo, che mi aveva creato delle bronchitasie sui polmoni
								, curata x fortuna in 5 lunghi anni , ma a tutt’ oggi porto ancora i segni di naso
								chiuso , abbassamenti di voce, respiro più affannoso nei giorni più umidi, ma da
								quando indosso la t-shirt nelle ore notturne al risveglio naso e fiato sono
								decisamente migliorati.
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Silvia (50 anni)</div>
								<div class="text-gray-600">Jesolo</div>
							</div>
						</figcaption>
					</figure>
				</div>
				<div class="space-y-8 xl:row-start-1">
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Ciao, stamattina appena sveglia dopo un sonno RILASSANTE, ho ricordato il sogno
								vivido e molto piacevole! Qualcosa mi suggeriva che deve essere accaduto qualcosa
								tra primo e secondo chakra. Sveglia ore 6 da due giorni e interruzione verso le due
								di notte, guardato la sveglia e riaddormentata subito.
							</p>
							<br />
							<p>Direi alla grande!</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Francesca (48 anni)</div>
								<div class="text-gray-600">Castelplanio</div>
							</div>
						</figcaption>
					</figure>

					<!-- More testimonials... -->
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Buongiorno! La maglietta L’ho indossata tutte le sere e devo dire che ho dormito
								sempre bene non svegliandomi mai durante il sonno, premetto che non ho grossi
								problemi nel dormire, pero’, la cosa che mi ha stupito di più e che mi sveglio
								serena, più tranquilla. Come anticipato, ricordo molto di più i sogni e comunque mi
								ci sono affezionata e quindi continuerò ad usarla e se scoprirò nuovi benefici vi
								informo. Un giorno nella pausa pranzo l’ho indossata perché avevo mal di stomaco e
								dopo un’ ora mi e’ passato, se dovesse ricapitare riprovo per avere conferma di
								questa cosa.
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Ida (38 anni)</div>
								<div class="text-gray-600">Pordenone</div>
							</div>
						</figcaption>
					</figure>

					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Ho avuto modo di conoscere ed apprezzare la maglietta “T-gravity” durante un
								incontro di presentazione.
							</p>
							<br />
							<p>
								La prima volta l’ho indossata per andare a dormire ho potuto notare un calore nella
								zona del petto corrispondente al Logo della maglietta. La notte ho dormito
								profondamente tanto che al mattino seguente mi sono svegliato più tardi del solito,
								normalmente mi sveglio sempre verso le ore 7 del mattino.
							</p>
							<br />
							<p>Quindi sonno profondo e sogni belli vividi ed intensi.</p>
							<br />
							<p>
								La cosa che mi ha sorpreso è stato quando mi sono recato al lavoro, premetto che
								sono un operatore olistico e faccio trattamenti e sono in continuo contatto con le
								persone, le volte precedenti rientravo a casa stanco ma queste ultime volte che
								utilizzavo alla notte la maglietta ero più attivo e meno stanco.
							</p>
							<br />
							<p>
								Da qui mi è venuta in mente un’idea: perché non indossare la maglietta durante il
								lavoro, i trattamenti?
							</p>
							<br />
							<p>Così ho fatto!</p>
							<br />
							<p>
								Ho potuto notare con sorpresa che mi sentivo sereno e meno affaticato, come se la
								“magica” maglietta mi Schermasse dalle negatività!
							</p>
							<br />
							<p>
								Posso assicurare che lavorare con più energia e meno stanchezza si è più attivi e
								sicuri nelle procedure.
							</p>
							<br />
							<p>
								Ne ho presa una seconda maglietta, per alternarla alla prima, vi aggiornerò se ci
								sono novità.
							</p>
							<br />
							<p>Grazie, Giorgio.</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Giorgio (58 anni)</div>
								<div class="text-gray-600">Conegliano</div>
							</div>
						</figcaption>
					</figure>
				</div>
			</div>
			<div class="space-y-8 xl:contents xl:space-y-0">
				<div class="space-y-8 xl:row-start-1">
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Ciao, ho indossato la maglietta “T-gravity” per andare a dormire per tre notti di
								seguito. Io di solito non dormo subito, leggo o faccio parole crociate. Appena
								coricata tutto normale, invece dopo una decina di minuti ho avvertito un grande
								calore, quasi un bruciore, sullo sterno (per tutta la sua lunghezza) e sulla colonna
								vertebrale, dall’ultima vertebra cervicale per tutte le dorsali.
							</p>
							<br />
							<p>
								Questa sensazione l’ho avvertita anche la sera dopo però meno intensa. La terza sera
								niente.
							</p>
							<br />
							<p>Adesso l’ho lavata e quando la rimetterò vi aggiornerò.</p>
							<br />
							<p>Grazie</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Donatella (60 anni)</div>
								<div class="text-gray-600">Sacile</div>
							</div>
						</figcaption>
					</figure>

					<!-- More testimonials... -->
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Nelle prime sere ho indossato la maglietta T-Gravity per andare a dormire, non l’ho
								messa durante il giorno perché sono presa da altri impegni non ho la giusta
								attenzione di quando vado a coricarmi, perché tu mi hai detto di fare attenzione se
								noto qualcosa. Prima di andare a coricarmi, di solito, mi siedo sul divano per
								guardare la Tv e mi addormento, poi mi alzo e vado a letto. Non riesco mai a
								riprendere subito il sonno e mi sveglio perché ho mille pensieri delle mie giornate
								piuttosto impegnative nel pensare a come fare per poter incastrare gli impegni
								quotidiani e mi faccio prendere dall’ansia per poter affrontare le varie
								problematiche. La prima sera, e le successive, ho indossato la maglietta ho avuto la
								sensazione che mi contenesse questa ansia e mi sentivo più tranquilla e serena, e
								come se mi avesse dato un po’ di calma interiore, avevo la sensazione che mi
								contenesse le mie preoccupazioni, effetto calmante, mi sono addormentata prima del
								solito. Questa è stata la mia esperienza con la maglietta T-Gravity.
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Erika (38 anni)</div>
								<div class="text-gray-600">Chions</div>
							</div>
						</figcaption>
					</figure>

					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Ho indossato la maglietta T-Gravity per un paio d’ore il primo giorno ed ho sentito
								un formicolio, un po’ di calore sul petto dove c’è il logo. Poi ho seguito il tuo
								consiglio è l’ho indossata per un pomeriggio intero…. Ed un paio di giorni a
								seguire….
							</p>
							<p>
								La notte ho dormito bene è profondamente, ho fatto un lungo sogno e me l’ho sono
								ricordato….
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Giulia (42 anni)</div>
								<div class="text-gray-600">Genova</div>
							</div>
						</figcaption>
					</figure>
				</div>
				<div class="space-y-8 xl:row-span-2">
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Ciao, devo dirvi che utilizzando la maglietta è stata una sensazione particolare:
								allora prima notte quando l’ho indossata ero molto stanca della giornata e quindi
								ero molto agitata e ho fatto fatica addormentarmi quindi non so sarà la maglietta
								sarà un po’ tutto l’insieme delle cose e invece poi l’ho messa un’altro paio di
								volte è andata veramente bene e mi sentivo molto bene.
							</p>
							<br />
							<p>
								Poi quando sono andata a camminare in montagna avevo la sensazione proprio di, non
								sospiegarla, ma proprio di tranquillità ecco a differenza della prima notte che io
								penso che fosse determinato la stanchezza invece usata in montagna mi dava pace e
								quindi queste sono quelle che ho provato io.
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Marinella (58 anni)</div>
								<div class="text-gray-600">Bolzano</div>
							</div>
						</figcaption>
					</figure>

					<!-- More testimonials... -->
					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>
								Ho usato la magliette di notte e mi sono addormentata subito e ho fatto dei sogni
								nitidi e al mattino me li ricordavo a differenza di sempre che al mattino me li
								dimenticatvo . Un’altra cosa che ho notato e stata che mi sveglio più volte durante
								la notte e poi fatico a riprendete il sonno , con la maglietta mi svegliavo comunque
								ma riprendevo subito il sonno . Mi alzo più rilassata.
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Gabriella (59 anni)</div>
								<div class="text-gray-600">Pordenone</div>
							</div>
						</figcaption>
					</figure>

					<figure class="rounded-2xl bg-white p-6 shadow-lg ring-1 ring-gray-900/5">
						<blockquote class="text-gray-900">
							<p>Ciao buongiorno</p>
							<p>
								Ti vorrei aggiornare in merito alle maglietta… È da una settimana circa che in
								merito alle problematiche e vicessitudini giornaliere (non è da me solitamente) che
								dico tutto ciò che non mi va, ciò che non mi sembra corretto, sia al lavoro che in
								famiglia senza imbarazzo e con convinzione…. Addirittura ho deciso di licenziarmi in
								quanto mi sono sentita scontata e mancata di rispetto e… Non so dirti ma mi sento
								completamente diversa… Non ho voglia di farmi schiacciare e non ho voglia di subire
								….. Poi ogni notte mi sveglio intorno alle 4 con la mente piena di pensieri e molto
								carica nel combattere per farmi valere. Non capisco più…. Io solitamente, per il
								quieto vivere faccio finta di niente, mando giù e vado oltre ma ora non riesco è
								come una ribellione interiore….
							</p>
						</blockquote>
						<figcaption class="mt-6 flex items-center gap-x-4">
							<div>
								<div class="font-semibold">Roberta (53 anni)</div>
								<div class="text-gray-600">Bolzano</div>
							</div>
						</figcaption>
					</figure>
				</div>
			</div>
		</div>
	</div>
</div>
