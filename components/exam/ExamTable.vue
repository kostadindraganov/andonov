<template>
	<div v-if="result.length > 0">


		<div class="text-center md:my-12 sm:my-10">
				<p class="md:text-5xl sm:text-4xl section-title font-boldCyrillic">
					ГРАФИК ИЗПИТИ
				</p>
			</div>
	<Card
		style="width: 100%; overflow: hidden"
		class="border-solid rounded-xl bg-stone bg-stoneBg bg-cover bg-no-repea"
	>
		<template #title>
			<!-- <h2 class="text-5xl text-white font-markscript text-center absolute m-auto left-0 right-0 mb-4 mx-2">
				{{ sheet }}
			</h2> -->
			<div class="flex justify-start  items-center font-bg text-white my-2  ">
						<p class="text-xl mr-4 text-left leading-7">
						Дата / Час
					</p>
					</div>
			<Divider />
		</template>
		<template #content>
			<div>
		<div v-for="(item, index) in result" key="index">
			<div
			v-if="item.length > 1"
				class="flex gap-2 justify-start items-center font-bg text-white my-2 mr-2"
			>
				<div>
					<p class="text-2xl text-center leading-7">
						{{ item[0] || "-" }} 
					</p>
					<p class="text-2xl text-center leading-7">
					{{ item[1] || "-" }}
					</p>
				</div>
				<Divider layout="vertical" />

				<div class="flex flex-row gap-2 flex-wrap justify-start items-center m-2 mr-2">
					<div v-for="indexes in 10" :key="indexes">
						<span class="text-xl text-left leading-7">
						{{ item[indexes+1]}} 
						</span>
						<span v-if="item.length > 2 && item[indexes+2]" class=" mr-2">,</span>
					</div>
				</div>
			
			</div>
			<Divider class="menu-divider" />
		</div>
	</div>			
		</template>
		<template #footer>
			<div class="flex gap-3 mt-1"></div>
		</template>
	</Card>
</div>
</template>

<script setup>
	import { reactive, computed } from "vue";

	const props = defineProps({
		sheet: String,
	});



	const headings = ref(null);
	const result = ref([]);
	const getVars = () => {
		const SPREAD_SHEET_ID = useRuntimeConfig().public.SPREAD_SHEET_ID;
		const GOOGLE_API_KEY = useRuntimeConfig().public.GOOGLE_API_KEY;

		return { SPREAD_SHEET_ID, GOOGLE_API_KEY };
	};
	const { SPREAD_SHEET_ID, GOOGLE_API_KEY } = getVars();
	const url = `https://sheets.googleapis.com/v4/spreadsheets/${SPREAD_SHEET_ID}/values/${
		props.sheet + "!A2:L40"
	}?key=${GOOGLE_API_KEY}`;

	const { data, error, refresh } = await useFetch(url, {
		onRequestError({ request, options, error }) {
			console.log(error);
  },
	onResponse({ request, response, options }) {
		console.log(response._data.values[0]);

	headings.value = response._data.values[0];
	result.value = [...response._data.values];
	console.log(result.value);
	}
	})
  

</script>
