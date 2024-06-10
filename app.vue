<template>
	<NuxtLayout>
		<main class="p-5 my-5">
			

			<div class="flex justify-center gap-5 flex-row flex-wrap my-5 pb-5">
				<ExamTable sheet="Изпити"  />
			</div>
		

			<div class="text-center md:my-12 sm:my-8">
				<p class="md:text-5xl sm:text-4xl section-title font-boldCyrillic">
					ГРАФИК КУРСОВЕ
				</p>
			</div>

		
		
			<div class="flex justify-center items-center gap-3 mt-14 mb-8">
				<p class="font-pacifico text-xl text-orange-500 mr-2">Сподели</p>
				<!-- Customization with props -->
				<SocialShare network="facebook" :styled="true" :label="false" />
				<SocialShare network="twitter" :styled="true" :label="false" />
				<SocialShare network="whatsapp" :styled="true" :label="false" />
				<SocialShare network="telegram" :styled="true" :label="false" />
			</div>
		</main>
	</NuxtLayout>
</template>

<script setup>
	useHead({
		title: "АНДОНОВ И СИН АВТОМОБИЛНА ШКОЛА ЕООД"
,
		meta: [
			{
				name: "description",
				ogImage: '~/assets/img/logo.png',
				content: "Шофьорски курсове Пазарджик АНДОНОВ И СИН АВТОМОБИЛНА ШКОЛА ЕООД има дългогодишен опит в обучението на водачи за управление на моторни превозни средства. Нашият екип ще ти предаде всички необходими знания и умения за твоята отлична подготовка. Ние ще те научим да бъдеш уверен и сигурен в своите способности при шофиране. При нас ще откриеш шофьорски курсове и обучение за следните категории: А1, A2, A, B, B+E, C, C+E, D",
			},
		],
	});
</script>

<style>
	.section-title {
		position: relative;
		display: inline-block;
		color: #f97316;
	}
	.section-title::after {
		position: absolute;
		content: "";
		width: 45px;
		height: 2px;
		top: 50%;
		right: -55px;
		margin-top: -1px;
		background: #f97316;
	}
	.section-title::before {
		position: absolute;
		content: "";
		width: 45px;
		height: 2px;
		top: 50%;
		left: -55px;
		margin-top: -1px;
		background: #f97316;
	}
</style>
