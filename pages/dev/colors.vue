<script setup>
// Демонстрация цветовой палитры
definePageMeta({
  title: 'Design System - Цвета'
})
</script>

<template>
	<DevPage
		title="Цветовая палитра"
		description="Цветовая система с поддержкой светлой и тёмной темы"
	>

			<!-- Основные цвета -->
			<section class="dev-section">
				<h2 class="h2">Основные цвета</h2>
				<p class="text-p text-secondary mb-lg">
					Брендовые цвета проекта
				</p>

				<div class="color-grid">
					<div class="color-card">
						<div class="color-card__preview primary"></div>
						<div class="color-card__info">
							<h3 class="h4">Primary</h3>
							<p class="text-sm text-secondary">Основной цвет</p>
							<code class="color-code">#0055ff</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview primary-hover"></div>
						<div class="color-card__info">
							<h3 class="h4">Primary Hover</h3>
							<p class="text-sm text-secondary">При наведении</p>
							<code class="color-code">#0041cc</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview secondary"></div>
						<div class="color-card__info">
							<h3 class="h4">Secondary</h3>
							<p class="text-sm text-secondary">Вторичный цвет</p>
							<code class="color-code">#ff6600</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview secondary-hover"></div>
						<div class="color-card__info">
							<h3 class="h4">Secondary Hover</h3>
							<p class="text-sm text-secondary">При наведении</p>
							<code class="color-code">#e65c00</code>
						</div>
					</div>
				</div>
			</section>

			<!-- Системные цвета -->
			<section class="dev-section">
				<h2 class="h2">Системные цвета</h2>
				<p class="text-p text-secondary mb-lg">
					Цвета для фона, текста и границ
				</p>

				<div class="color-grid">
					<div class="color-card">
						<div class="color-card__preview background"></div>
						<div class="color-card__info">
							<h3 class="h4">Background</h3>
							<p class="text-sm text-secondary">Основной фон</p>
							<code class="color-code">#ffffff</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview surface"></div>
						<div class="color-card__info">
							<h3 class="h4">Surface</h3>
							<p class="text-sm text-secondary">Поверхности</p>
							<code class="color-code">#f9f9f9</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview text"></div>
						<div class="color-card__info">
							<h3 class="h4">Text</h3>
							<p class="text-sm text-secondary">Основной текст</p>
							<code class="color-code">#1a1a1a</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview text-secondary"></div>
						<div class="color-card__info">
							<h3 class="h4">Text Secondary</h3>
							<p class="text-sm text-secondary">Вторичный текст</p>
							<code class="color-code">#4d4d4d</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview border"></div>
						<div class="color-card__info">
							<h3 class="h4">Border</h3>
							<p class="text-sm text-secondary">Границы</p>
							<code class="color-code">#e0e0e0</code>
						</div>
					</div>
				</div>
			</section>

			<!-- Статусные цвета -->
			<section class="dev-section">
				<h2 class="h2">Статусные цвета</h2>
				<p class="text-p text-secondary mb-lg">
					Цвета для отображения состояний
				</p>

				<div class="color-grid">
					<div class="color-card">
						<div class="color-card__preview success"></div>
						<div class="color-card__info">
							<h3 class="h4">Success</h3>
							<p class="text-sm text-secondary">Успех</p>
							<code class="color-code">#28a745</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview warning"></div>
						<div class="color-card__info">
							<h3 class="h4">Warning</h3>
							<p class="text-sm text-secondary">Предупреждение</p>
							<code class="color-code">#ffc107</code>
						</div>
					</div>

					<div class="color-card">
						<div class="color-card__preview error"></div>
						<div class="color-card__info">
							<h3 class="h4">Error</h3>
							<p class="text-sm text-secondary">Ошибка</p>
							<code class="color-code">#dc3545</code>
						</div>
					</div>
				</div>
			</section>

			<!-- Примеры использования -->
			<section class="dev-section">
				<h2 class="h2">Примеры использования</h2>
				<div class="usage-examples">
					<div class="usage-example">
						<h3 class="h4">Кнопки</h3>
						<div class="button-examples">
							<button class="btn btn-primary">Primary Button</button>
							<button class="btn btn-secondary">Secondary Button</button>
							<button class="btn btn-success">Success Button</button>
							<button class="btn btn-warning">Warning Button</button>
							<button class="btn btn-error">Error Button</button>
						</div>
					</div>

					<div class="usage-example">
						<h3 class="h4">Алерты</h3>
						<div class="alert-examples">
							<div class="alert alert-success">
								<strong>Успех!</strong> Операция выполнена успешно.
							</div>
							<div class="alert alert-warning">
								<strong>Внимание!</strong> Проверьте введённые данные.
							</div>
							<div class="alert alert-error">
								<strong>Ошибка!</strong> Что-то пошло не так.
							</div>
						</div>
					</div>
				</div>
			</section>

			<!-- CSS переменные -->
			<section class="dev-section">
				<h2 class="h2">CSS переменные</h2>
				<div class="code-example">
					<pre class="code-block"><code>/* Использование в CSS */
.my-element {
  background-color: var(--color-primary);
  color: var(--color-text);
  border: 1px solid var(--color-border);
}

/* Использование в SCSS */
.my-component {
  background: var(--color-surface);
  padding: var(--spacing-md);
}</code></pre>
				</div>
			</section>
	</DevPage>
</template>

<style lang="scss" scoped>
@use "~/assets/styles/variables/index" as *;
@use "~/assets/styles/base/mixins" as *;

.dev-section {
	margin-bottom: var(--spacing-xxl);
}

.color-grid {
	@include responsive-grid(1, 2, 4);
	gap: var(--spacing-lg);
	margin-top: var(--spacing-lg);
}

.color-card {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	overflow: hidden;
	transition: transform 0.3s ease;

	&:hover {
		transform: translateY(-2px);
	}
}

.color-card__preview {
	height: 120px;
	width: 100%;
	
	&.primary { background-color: var(--color-primary); }
	&.primary-hover { background-color: var(--color-primary-hover); }
	&.secondary { background-color: var(--color-secondary); }
	&.secondary-hover { background-color: var(--color-secondary-hover); }
	&.background { background-color: var(--color-background); border: 1px solid var(--color-border); }
	&.surface { background-color: var(--color-surface); }
	&.text { background-color: var(--color-text); }
	&.text-secondary { background-color: var(--color-text-secondary); }
	&.border { background-color: var(--color-border); }
	&.success { background-color: var(--color-success); }
	&.warning { background-color: var(--color-warning); }
	&.error { background-color: var(--color-error); }
}

.color-card__info {
	padding: var(--spacing-lg);
}

.color-code {
	display: block;
	margin-top: var(--spacing-sm);
	font-family: 'Courier New', monospace;
	font-size: 0.875rem;
	background-color: var(--color-surface);
	padding: var(--spacing-xs) var(--spacing-sm);
	border-radius: 4px;
	color: var(--color-text-secondary);
}

.mb-lg { margin-bottom: var(--spacing-lg); }

.usage-examples {
	@include responsive-grid(1, 1, 2);
	gap: var(--spacing-xl);
	margin-top: var(--spacing-lg);
}

.usage-example {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
}

.button-examples {
	display: flex;
	flex-wrap: wrap;
	gap: var(--spacing-md);
	margin-top: var(--spacing-md);
}

.btn {
	padding: var(--spacing-sm) var(--spacing-lg);
	border: none;
	border-radius: 4px;
	font-size: 0.875rem;
	font-weight: 500;
	cursor: pointer;
	transition: all 0.3s ease;

	&.btn-primary {
		background-color: var(--color-primary);
		color: white;
		&:hover { background-color: var(--color-primary-hover); }
	}

	&.btn-secondary {
		background-color: var(--color-secondary);
		color: white;
		&:hover { background-color: var(--color-secondary-hover); }
	}

	&.btn-success {
		background-color: var(--color-success);
		color: white;
		&:hover { opacity: 0.8; }
	}

	&.btn-warning {
		background-color: var(--color-warning);
		color: var(--color-text);
		&:hover { opacity: 0.8; }
	}

	&.btn-error {
		background-color: var(--color-error);
		color: white;
		&:hover { opacity: 0.8; }
	}
}

.alert-examples {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-md);
	margin-top: var(--spacing-md);
}

.alert {
	padding: var(--spacing-md);
	border-radius: 4px;
	border-left: 4px solid;

	&.alert-success {
		background-color: rgba(40, 167, 69, 0.1);
		border-left-color: var(--color-success);
		color: var(--color-success);
	}

	&.alert-warning {
		background-color: rgba(255, 193, 7, 0.1);
		border-left-color: var(--color-warning);
		color: #856404;
	}

	&.alert-error {
		background-color: rgba(220, 53, 69, 0.1);
		border-left-color: var(--color-error);
		color: var(--color-error);
	}
}

.code-example {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
}

.code-block {
	background-color: #1e1e1e;
	color: #d4d4d4;
	padding: var(--spacing-lg);
	border-radius: 4px;
	overflow-x: auto;
	font-family: 'Courier New', monospace;
	font-size: 0.875rem;
	line-height: 1.5;
	margin: 0;
}
</style>