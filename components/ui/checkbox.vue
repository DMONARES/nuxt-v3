<script setup>
	// props
	const props = defineProps({
		value: {
			type: Boolean,
			default: false,
		},
		error: {
			type: Boolean,
			default: false,
		},
	});

	// emits
	const emit = defineEmits(['update:value']);

	// functions
	const updateValue = () => {
		emit('update:value', props.value ? false : true);
	}
</script>

<template>
	<label class="ui-checkbox" :class="{'error': error}">
		<input
			type="checkbox"
			:value="value"
			@input="updateValue"
		/>
		<div class="ui-checkbox__checkbox" :class="{'active': value}">
			<icons-checked v-if="value" />
		</div>
		<span class="ui-checkbox__label">
			<slot />
		</span>
	</label>
</template>

<style lang="scss" scoped>
@use "~/assets/styles/variables/index" as *;
@use "~/assets/styles/base/mixins" as *;

.ui-checkbox {
	cursor: pointer;
	display: flex;
	gap: 12px;
	align-items: center;

	input { display: none; }
	&.error {
		.ui-checkbox__checkbox { border-color: var(--color-error) }
		.ui-checkbox__label { color: var(--color-error) }
	}
}

.ui-checkbox__checkbox {
	border: 2px solid var(--color-border);
	width: 24px;
	height: 24px;
	border-radius: 4px;

	display: flex;
	align-items: center;
	justify-content: center;
	@include transition();

	&.active
	{
		background-color: var(--color-primary);
		border-color: var(--color-primary);
	}
}

.ui-checkbox__label {
	font-size: 1rem;
	color: var(--color-text);

	a {
		color: inherit;
		text-decoration: underline;
	}
}
</style>