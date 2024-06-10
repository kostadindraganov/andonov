<template>
	<MegaMenu
		:unstyled="false"
		class="pt-2 px-5 mt-5 surface-0 flex flex-row align-items-center justify-between"
	>
		<template #start class="mr-5">
			<img
				src="~/assets/img/logo.png"
				class="h-12 me-3 rounded-xl"
				alt="andonov Logo"
			/>
		</template>
		<template #end>
			<a href="tel:0885876585">
				<Button
					rounded
					class="order-btn"
					type="button"
					label="ОБАДИ СЕ"
					icon="pi pi-phone"
					severity="warning"
				/>
			</a>
		</template>
	</MegaMenu>
	<img src="~/assets/img/bg11.jpg" class="w-full me-3" alt="hero Logo" />

</template>

<style scoped>
	.p-megamenu {
		width: 100%;
		position: absolute;
		background-color: transparent;
		z-index: 20;
		border: none;
	}
	.order-btn {
		background-color: white;
		border: none;
		color: #f97316;
		font-size: 12px;
	}
</style>
