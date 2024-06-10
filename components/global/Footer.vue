<template>
	<footer class="bg-white dark:bg-gray-900 bg-footer bg-cover bg-no-repeat">
		<div class="mx-auto w-full max-w-screen-xl p-4 py-6 lg:py-8">
			<div class="md:flex md:justify-between items-center">
				<div class="mb-6 md:mb-0">
					<a href="https://andonov.netlify.app/" class="flex items-center">
						<img
							src="~/assets/img/logo.png"
							class="sm:w-24 md:w-52 me-3 rounded-3xl"
							alt="FlowBite Logo"
						/>
					</a>
				</div>
				<div
					class="flex flex-wrap justify-center items-center gap-8 sm:gap-6 sm:grid-cols-3"
				>
					<div></div>

					<div class="font-bg text-center">
						<h2
							class="mb-6 text-sm font-boldCyrillic font-semibold text-orange-500 uppercase"
						>
							ЗА КОНТАКТ
						</h2>
						<ul class="text-white text-lg font-medium">
							<li class="mb-4">
								<p>гр.Пазарджик</p>
								<p>УЛ. "ХРИСТО СМИРНЕНСКИ" № 26/4</p>
							</li>
							<li>
								<p>0885 / 876 585</p>
							</li>
							<li>
								<a href="tel:0885876585">
									<Button
										rounded
										class="my-5 border-none"
										type="button"
										label="Обади се"
										icon="pi pi-phone"
										severity="warning"
									/>
								</a>
							</li>
						</ul>
					</div>
				</div>
			</div>
			<hr
				class="my-6 border-gray-700 sm:mx-auto dark:border-gray-700 lg:my-8"
			/>
			<div class="sm:flex sm:items-center sm:justify-between">
				<span class="text-md font-bg text-white text-center"
					>
					"АНДОНОВ И СИН АВТОМОБИЛНА ШКОЛА" ЕООД има дългогодишен опит в обучението на водачи за управление на моторни превозни средства. Нашият екип ще ти предаде всички необходими знания и умения за твоята отлична подготовка. Ние ще те научим да бъдеш уверен и сигурен в своите способности при шофиране. При нас ще откриеш шофьорски курсове и обучение за следните категории: А1, A2, A, B, B+E, C, C+E, D
				</span>
				<!-- <div class="flex mt-4 mr-4 sm:justify-center sm:mt-0">
					<a
						href="#"
						class="text-white hover:text-gray-900 dark:hover:text-white"
					>
						<svg
							class="w-4 h-4"
							aria-hidden="true"
							xmlns="http://www.w3.org/2000/svg"
							fill="currentColor"
							viewBox="0 0 8 19"
						>
							<path
								fill-rule="evenodd"
								d="M6.135 3H8V0H6.135a4.147 4.147 0 0 0-4.142 4.142V6H0v3h2v9.938h3V9h2.021l.592-3H5V3.591A.6.6 0 0 1 5.592 3h.543Z"
								clip-rule="evenodd"
							/>
						</svg>
						<span class="sr-only">Facebook page</span>
					</a>
				</div> -->
			</div>
		</div>
	</footer>
</template>

<script setup></script>
