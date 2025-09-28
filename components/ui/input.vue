<script setup>
	const props = defineProps({
		type       : { type: String, default : 'text', },
		value      : { type: String, required: true },
		label      : { type: String, default : '' },
		placeholder: { type: String, default : '' },
		errorText  : { type: String, default: '' },
		error      : { type: Boolean, default: false },
		disabled   : { type: Boolean, default: false },
		isPhone    : { type: Boolean, default: false },
	});
	const emit = defineEmits(['update:value', 'triggerIcon']);

	// vars
	const focus = ref(false);
	const inputRef = ref(null);

	// functions
	const focusInput = () => {
		if (inputRef.value)
			inputRef.value.focus();
	};
	const updateValue = (value) => emit('update:value', value);

	// check hasSlot
	const slots = useSlots()
	const hasSlotContent = slots.hasOwnProperty('default') && slots.default().length > 0
</script>

<template>
	<div
		class="ui-input"
		:class="{
			'active': focus || value,
			'disabled': disabled,
			'error': error,
		}"
	>
		<label
			v-if="label"
			class="ui-input__label"
			@click="focusInput"
		>
			{{ label }}
		</label>

		<div class="ui-input__wr">
			<input
				v-if="!isPhone"
				class="ui-input__input"
				ref="inputRef"
				:type="type"
				:value="value"
				:placeholder="placeholder"
				:disabled="disabled"
				@focus="focus = true"
				@blur="focus = false"
				@input="updateValue($event.target.value)"
			>
			<input
				v-else
				class="ui-input__input"
				ref="inputRef"
				v-maska
				data-maska="+7 (###) ###-##-##"
				:type="type"
				:value="value"
				:placeholder="placeholder"
				:disabled="disabled"
				@focus="focus = true"
				@blur="focus = false"
				@input="updateValue($event.target.value)"
			>
			<div v-if="hasSlotContent" class="ui-input__icon" @click="emit('triggerIcon')">
				<slot /> 
			</div>
		</div>

		<span v-if="errorText" class="ui-input__error-text">{{ errorText }}</span>
	</div>
</template>

<style lang="scss" scoped>
@use "~/assets/styles/variables/index" as *;
@use "~/assets/styles/base/mixins" as *;

.ui-input
{
	&.active
	{
		.ui-input__input { border-color: var(--color-primary); }
	}

	&.error
	{
		.ui-input__input { border-color: var(--color-error); }
	}

	&.disabled { cursor: not-allowed; }
}

.ui-input__wr { position: relative; }

.ui-input__label
{
	width: max-content;
	display: block;
	margin-bottom: 5px;
	cursor: pointer;
	font-size: 1rem;
	font-weight: 500;
	color: var(--color-text);

	@include transition();
}

.ui-input__input
{
	// default
	width: 100%;
	padding: 12px 16px;
	border: 2px solid var(--color-border);
	outline: none;
	border-radius: 6px;
	background-color: var(--color-surface);
	color: var(--color-text);
	font-size: 1rem;
	@include transition();

	// effects
	&:hover { border-color: var(--color-primary); }
	&::placeholder { color: var(--color-text-secondary); }
	&:disabled
	{
		pointer-events: none;
		opacity: .5;
	}
}

.ui-input__error-text
{
	display: block;
	margin-top: 5px;
	color: var(--color-error);
	font-size: .75rem;
}

.ui-input__icon
{
	cursor: pointer;
	position: absolute;
	top: 50%;
	transform: translateY(-50%);
	right: 10px;
	line-height: 0;
	overflow: hidden;

	svg
	{
		width: 16px;
		height: 16px;
	}
}
</style>