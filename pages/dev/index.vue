<script setup>
// Главная страница документации
definePageMeta({
  title: 'Design System - Главная'
})
</script>

<template>
	<div class="dev-page">
		<div class="container">
			<div class="dev-header">
				<h1 class="h1">Design System</h1>
				<p class="text-p text-secondary">
					Документация по стилям и компонентам проекта
				</p>
			</div>

			<div class="dev-grid">
				<NuxtLink to="/dev/colors" class="dev-card">
					<div class="dev-card__icon">
						<div class="color-preview primary"></div>
						<div class="color-preview secondary"></div>
						<div class="color-preview success"></div>
					</div>
					<div class="dev-card__content">
						<h3 class="h4">Цвета</h3>
						<p class="text-sm text-secondary">
							Цветовая палитра проекта с поддержкой светлой и тёмной темы
						</p>
					</div>
				</NuxtLink>

				<NuxtLink to="/dev/typography" class="dev-card">
					<div class="dev-card__icon">
						<div class="typography-preview">
							<span class="h6">Aa</span>
						</div>
					</div>
					<div class="dev-card__content">
						<h3 class="h4">Типографика</h3>
						<p class="text-sm text-secondary">
							Шрифты, размеры, веса и адаптивная типографика
						</p>
					</div>
				</NuxtLink>

				<NuxtLink to="/dev/ui" class="dev-card">
					<div class="dev-card__icon">
						<div class="ui-preview">
							<div class="ui-preview__button"></div>
							<div class="ui-preview__input"></div>
						</div>
					</div>
					<div class="dev-card__content">
						<h3 class="h4">UI Компоненты</h3>
						<p class="text-sm text-secondary">
							Кнопки, поля ввода, чекбоксы и другие элементы интерфейса
						</p>
					</div>
				</NuxtLink>

				<NuxtLink to="/dev/utils" class="dev-card">
					<div class="dev-card__icon">
						<div class="utils-preview">
							<div class="utils-preview__item"></div>
							<div class="utils-preview__item"></div>
							<div class="utils-preview__item"></div>
						</div>
					</div>
					<div class="dev-card__content">
						<h3 class="h4">Утилиты</h3>
						<p class="text-sm text-secondary">
							Миксины, хелперы и вспомогательные классы
						</p>
					</div>
				</NuxtLink>

			</div>
		</div>
	</div>
</template>

<style lang="scss" scoped>
@use "~/assets/styles/variables/index" as *;
@use "~/assets/styles/base/mixins" as *;

.dev-page {
	min-height: 100vh;
	background-color: var(--color-background);
	padding: var(--spacing-xxl) 0;
}

.dev-header {
	text-align: center;
	margin-bottom: var(--spacing-xxl);
}

.dev-grid {
	@include responsive-grid(1, 2, 3);
	max-width: 1000px;
	margin: 0 auto;
}

.dev-card {
	display: block;
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 12px;
	padding: var(--spacing-xl);
	text-decoration: none;
	color: inherit;
	transition: all 0.2s ease;
	height: 100%;
	position: relative;
	overflow: hidden;

	&::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background: linear-gradient(135deg, var(--color-primary), var(--color-secondary));
		opacity: 0;
		transition: opacity 0.2s ease;
		z-index: 0;
	}

	&:hover {
		border-color: var(--color-primary);
		box-shadow: 0 4px 20px rgba(37, 99, 235, 0.15);
		
		&::before {
			opacity: 0.05;
		}
	}

	&:active {
		transform: scale(0.98);
	}
}

.dev-card__icon {
	display: flex;
	align-items: center;
	justify-content: center;
	height: 80px;
	margin-bottom: var(--spacing-lg);
	position: relative;
	z-index: 1;
}

.dev-card__content {
	text-align: center;
	position: relative;
	z-index: 1;
}

// Превью для цветов
.color-preview {
	width: 20px;
	height: 20px;
	border-radius: 50%;
	margin: 0 4px;
	
	&.primary { background-color: var(--color-primary); }
	&.secondary { background-color: var(--color-secondary); }
	&.success { background-color: var(--color-success); }
}

// Превью для типографики
.typography-preview {
	display: flex;
	align-items: center;
	justify-content: center;
	width: 60px;
	height: 60px;
	background-color: var(--color-primary);
	color: white;
	border-radius: 8px;
	font-weight: 700;
}

// Превью для UI
.ui-preview {
	display: flex;
	flex-direction: column;
	gap: 8px;
	align-items: center;
}

.ui-preview__button {
	width: 60px;
	height: 24px;
	background-color: var(--color-primary);
	border-radius: 4px;
}

.ui-preview__input {
	width: 80px;
	height: 20px;
	border: 2px solid var(--color-border);
	border-radius: 4px;
}

// Превью для утилит
.utils-preview {
	display: flex;
	gap: 4px;
	align-items: center;
}

.utils-preview__item {
	width: 12px;
	height: 12px;
	background-color: var(--color-primary);
	border-radius: 2px;
}

// Превью для иконок
.icons-preview {
	display: flex;
	align-items: center;
	justify-content: center;
	width: 60px;
	height: 60px;
	background-color: var(--color-surface);
	border: 2px solid var(--color-border);
	border-radius: 8px;
	color: var(--color-primary);
}
</style>