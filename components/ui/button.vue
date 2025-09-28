<script setup>
	const props = defineProps({
		variant: String, // default, border
		size: String, // default, xl
		disabled: Boolean,
	});
</script>

<template>
	<button
		class="ui-button"
		:class="{
			'border': variant === 'border',
			'xl': size === 'xl',
		}"
		:disabled="disabled"
	>
		<slot />
	</button>
</template>

<style lang="scss" scoped>
@use "~/assets/styles/variables/index" as *;
@use "~/assets/styles/base/mixins" as *;

.ui-button
{
	// base styles
	cursor: pointer;
	border: none;
	padding: 12px 24px;
	border: 1px solid transparent;
	border-radius: 6px;
	background-color: var(--color-primary);
	color: white;
	font-size: 1rem;
	font-weight: 500;

	@include transition();

	// effects
	&:disabled
	{
		pointer-events: none;
		opacity: .7;
	}
	&:hover { 
		background-color: var(--color-primary-hover);
	}

	// sizes
	&.xl { padding: 20px 64px; }

	// variants
	&.border
	{
		background-color: transparent;
		border-color: var(--color-primary);
		color: var(--color-primary);

		&:hover
		{
			background-color: var(--color-primary);
			color: white;
		}
	}
}
</style>