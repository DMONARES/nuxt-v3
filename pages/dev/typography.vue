<script setup>
// Демонстрация типографики
definePageMeta({
  title: 'Design System - Типографика'
})
</script>

<template>
	<DevPage
		title="Типографика"
		description="Система шрифтов, размеров и адаптивной типографики"
	>

			<!-- Заголовки -->
			<section class="dev-section">
				<h2 class="h2">Заголовки</h2>
				<p class="text-p text-secondary mb-lg">
					Адаптивные заголовки с fluid typography
				</p>

				<div class="typography-examples">
					<div class="typography-example">
						<h1 class="h1">Заголовок H1</h1>
						<p class="text-sm text-secondary">clamp(1.75rem, 4vw, 2.5rem) • 28px - 40px</p>
					</div>

					<div class="typography-example">
						<h2 class="h2">Заголовок H2</h2>
						<p class="text-sm text-secondary">clamp(1.5rem, 3.5vw, 2rem) • 24px - 32px</p>
					</div>

					<div class="typography-example">
						<h3 class="h3">Заголовок H3</h3>
						<p class="text-sm text-secondary">clamp(1.25rem, 3vw, 1.75rem) • 20px - 28px</p>
					</div>

					<div class="typography-example">
						<h4 class="h4">Заголовок H4</h4>
						<p class="text-sm text-secondary">clamp(1.125rem, 2.5vw, 1.5rem) • 18px - 24px</p>
					</div>

					<div class="typography-example">
						<h5 class="h5">Заголовок H5</h5>
						<p class="text-sm text-secondary">clamp(1rem, 2vw, 1.25rem) • 16px - 20px</p>
					</div>

					<div class="typography-example">
						<h6 class="h6">Заголовок H6</h6>
						<p class="text-sm text-secondary">clamp(0.875rem, 1.5vw, 1rem) • 14px - 16px</p>
					</div>
				</div>
			</section>

			<!-- Размеры текста -->
			<section class="dev-section">
				<h2 class="h2">Размеры текста</h2>
				<p class="text-p text-secondary mb-lg">
					Адаптивные размеры текста для различного контента
				</p>

				<div class="text-sizes">
					<div class="text-size-example">
						<p class="text-xs">Очень маленький текст (12px)</p>
						<code class="text-code">.text-xs</code>
					</div>

					<div class="text-size-example">
						<p class="text-sm">Маленький текст (14px)</p>
						<code class="text-code">.text-sm</code>
					</div>

					<div class="text-size-example">
						<p class="text-base">Базовый текст (16px)</p>
						<code class="text-code">.text-base</code>
					</div>

					<div class="text-size-example">
						<p class="text-lg">Большой текст (18px)</p>
						<code class="text-code">.text-lg</code>
					</div>

					<div class="text-size-example">
						<p class="text-xl">Очень большой текст (20px)</p>
						<code class="text-code">.text-xl</code>
					</div>
				</div>
			</section>

			<!-- Цвета текста -->
			<section class="dev-section">
				<h2 class="h2">Цвета текста</h2>
				<p class="text-p text-secondary mb-lg">
					Семантические цвета для текста
				</p>

				<div class="text-colors">
					<div class="text-color-example">
						<p class="text-primary">Основной текст</p>
						<code class="text-code">.text-primary</code>
					</div>

					<div class="text-color-example">
						<p class="text-secondary">Вторичный текст</p>
						<code class="text-code">.text-secondary</code>
					</div>

					<div class="text-color-example">
						<p class="text-success">Успешный текст</p>
						<code class="text-code">.text-success</code>
					</div>

					<div class="text-color-example">
						<p class="text-warning">Предупреждающий текст</p>
						<code class="text-code">.text-warning</code>
					</div>

					<div class="text-color-example">
						<p class="text-error">Ошибочный текст</p>
						<code class="text-code">.text-error</code>
					</div>

					<div class="text-color-example">
						<p class="text-link">Ссылочный текст</p>
						<code class="text-code">.text-link</code>
					</div>
				</div>
			</section>

			<!-- Примеры контента -->
			<section class="dev-section">
				<h2 class="h2">Примеры контента</h2>
				<p class="text-p text-secondary mb-lg">
					Реальные примеры использования типографики
				</p>

				<div class="content-examples">
					<div class="content-example">
						<h3 class="h3">Статья</h3>
						<div class="article-content">
							<h1 class="h1">Заголовок статьи</h1>
							<p class="text-p">
								Это пример основного текста статьи. Он использует базовый размер шрифта и оптимальную высоту строки для лучшей читаемости. Адаптивная типографика автоматически подстраивается под размер экрана.
							</p>
							<h2 class="h2">Подзаголовок</h2>
							<p class="text-p">
								Вторичный текст может быть использован для дополнительной информации или описаний. Он имеет меньший размер и более светлый цвет.
							</p>
							<p class="text-sm text-secondary">
								Мелкий текст подходит для подписей, дат и дополнительной информации.
							</p>
						</div>
					</div>

					<div class="content-example">
						<h3 class="h3">Карточка продукта</h3>
						<div class="product-card">
							<h4 class="h4">Название продукта</h4>
							<p class="text-p text-secondary">Краткое описание продукта</p>
							<div class="product-price">
								<span class="h5 text-primary">1 299 ₽</span>
								<span class="text-sm text-secondary">за штуку</span>
							</div>
							<button class="btn btn-primary">Купить</button>
						</div>
					</div>
				</div>
			</section>

			<!-- Адаптивность -->
			<section class="dev-section">
				<h2 class="h2">Адаптивность</h2>
				<p class="text-p text-secondary mb-lg">
					Типографика автоматически адаптируется под размер экрана
				</p>

				<div class="responsive-demo">
					<div class="responsive-item">
						<h4 class="h4">Мобильные устройства</h4>
						<p class="text-sm text-secondary">Базовый размер: 14px</p>
						<div class="mobile-preview">
							<h1 class="h1">Заголовок</h1>
							<p class="text-p">Текст на мобильном</p>
						</div>
					</div>

					<div class="responsive-item">
						<h4 class="h4">Планшеты</h4>
						<p class="text-sm text-secondary">Базовый размер: 16px</p>
						<div class="tablet-preview">
							<h1 class="h1">Заголовок</h1>
							<p class="text-p">Текст на планшете</p>
						</div>
					</div>

					<div class="responsive-item">
						<h4 class="h4">Десктоп</h4>
						<p class="text-sm text-secondary">Базовый размер: 18px</p>
						<div class="desktop-preview">
							<h1 class="h1">Заголовок</h1>
							<p class="text-p">Текст на десктопе</p>
						</div>
					</div>
				</div>
			</section>

			<!-- CSS переменные -->
			<section class="dev-section">
				<h2 class="h2">CSS переменные</h2>
				<div class="code-example">
					<pre class="code-block"><code>/* Использование в HTML */
&lt;h1 class="h1"&gt;Заголовок&lt;/h1&gt;
&lt;p class="text-p text-secondary"&gt;Текст&lt;/p&gt;

/* Использование в CSS */
.my-heading {
  font-size: var(--font-size-h1);
  line-height: var(--line-height-h1);
  font-weight: 700;
}

.my-text {
  font-size: var(--font-size-base);
  line-height: var(--line-height-base);
  color: var(--color-text-secondary);
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

.typography-examples {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-lg);
	margin-top: var(--spacing-lg);
}

.typography-example {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
}

.text-sizes {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-md);
	margin-top: var(--spacing-lg);
}

.text-size-example {
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: var(--spacing-md);
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
}

.text-code {
	font-family: 'Courier New', monospace;
	font-size: 0.875rem;
	background-color: var(--color-background);
	padding: var(--spacing-xs) var(--spacing-sm);
	border-radius: 4px;
	color: var(--color-text-secondary);
}

.text-colors {
	@include responsive-grid(1, 2, 3);
	gap: var(--spacing-md);
	margin-top: var(--spacing-lg);
}

.text-color-example {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
	text-align: center;
}

.content-examples {
	@include responsive-grid(1, 1, 2);
	gap: var(--spacing-xl);
	margin-top: var(--spacing-lg);
}

.content-example {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
}

.article-content {
	max-width: 600px;
}

.product-card {
	background-color: var(--color-background);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
	max-width: 300px;
}

.product-price {
	display: flex;
	align-items: baseline;
	gap: var(--spacing-sm);
	margin: var(--spacing-md) 0;
}

.btn {
	padding: var(--spacing-sm) var(--spacing-lg);
	background-color: var(--color-primary);
	color: white;
	border: none;
	border-radius: 4px;
	font-size: 0.875rem;
	font-weight: 500;
	cursor: pointer;
	transition: all 0.3s ease;

	&:hover {
		background-color: var(--color-primary-hover);
	}
}

.responsive-demo {
	@include responsive-grid(1, 1, 3);
	gap: var(--spacing-lg);
	margin-top: var(--spacing-lg);
}

.responsive-item {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
	text-align: center;
}

.mobile-preview,
.tablet-preview,
.desktop-preview {
	background-color: var(--color-background);
	border: 1px solid var(--color-border);
	border-radius: 4px;
	padding: var(--spacing-md);
	margin-top: var(--spacing-md);
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

.mb-lg { margin-bottom: var(--spacing-lg); }
</style>