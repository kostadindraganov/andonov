<template>
	<div v-if="data.length > 1">
		<div v-for="(item, index) in result" key="index">
			<div
			v-if="item.length > 1"
			
				class="flex justify-between items-center font-bg text-white my-2 "
			>
				<div>
					<p class="text-3xl text-left leading-7 m-2 ">
						{{ item[0] || "-" }}
					</p>
				
				</div>
	
				<div class="flex flex-col justify-center items-center">
					<div v-for="indexes in 10" :key="indexes">
						<span class="lg:text-2xl sm:text-xl text-left leading-7">
						{{ item[indexes]  }}
						</span>
						<span v-if="item.length > 2 && item[indexes+1]" class=" mr-2">,</span>

					</div>
				</div>
			
			</div>
			<Divider class="menu-divider" />
		</div>
	</div>
	<Skeleton v-else width="100%" height="150px"></Skeleton>
</template>

<script setup>
	import { reactive, computed } from "vue";


	const props = defineProps({
		result: {
			type: Array,
			required: true,
			default: [],
		},
	});
	const data = computed(() => props.result || []);

</script>

<style scoped>
	.p-divider.p-divider-horizontal {
		margin: 0px;
	}
	.menu-divider.p-divider-horizontal:before {
		border-top: 1px solid #484a4c;
	}
</style>
