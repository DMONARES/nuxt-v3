<script setup>
// Демонстрация утилит и миксинов
definePageMeta({
  title: 'Design System - Утилиты'
})
</script>

<template>
	<DevPage
		title="Утилиты и Миксины"
		description="Вспомогательные классы, миксины и утилиты для быстрой разработки"
	>

			<!-- Контейнеры -->
			<section class="dev-section">
				<h2 class="h2">Контейнеры</h2>
				<p class="text-p text-secondary mb-lg">
					Адаптивные контейнеры для различного контента
				</p>

				<div class="dev-examples">
					<div class="dev-example">
						<h3 class="h4">.container</h3>
						<p class="text-sm text-secondary mb-md">
							Основной контейнер с максимальной шириной 1200px
						</p>
						<div class="container demo-container">
							<p class="text-p">Содержимое контейнера</p>
						</div>
					</div>

					<div class="dev-example">
						<h3 class="h4">.container-narrow</h3>
						<p class="text-sm text-secondary mb-md">
							Узкий контейнер (800px) для лучшей читаемости
						</p>
						<div class="container-narrow demo-container">
							<p class="text-p">Узкий контейнер для текста</p>
						</div>
					</div>

					<div class="dev-example">
						<h3 class="h4">.container-center</h3>
						<p class="text-sm text-secondary mb-md">
							Центрированный контейнер по горизонтали и вертикали
						</p>
						<div class="container-center demo-container-center">
							<p class="text-p">Центрированный контент</p>
						</div>
					</div>
				</div>
			</section>

			<!-- Адаптивная видимость -->
			<section class="dev-section">
				<h2 class="h2">Адаптивная видимость</h2>
				<p class="text-p text-secondary mb-lg">
					Классы для показа/скрытия элементов на разных устройствах
				</p>

				<div class="dev-examples">
					<div class="dev-example">
						<h3 class="h4">Видимость по устройствам</h3>
						<div class="visibility-demo">
							<div class="visibility-item visible-mobile">
								<span class="text-sm">Только мобильные</span>
							</div>
							<div class="visibility-item visible-tablet">
								<span class="text-sm">Только планшеты</span>
							</div>
							<div class="visibility-item visible-desktop">
								<span class="text-sm">Только десктоп</span>
							</div>
						</div>
					</div>
				</div>
			</section>

			<!-- Миксины -->
			<section class="dev-section">
				<h2 class="h2">Миксины</h2>
				<p class="text-p text-secondary mb-lg">
					SCSS миксины для быстрой разработки
				</p>

				<div class="dev-examples">
					<div class="dev-example">
						<h3 class="h4">Flexbox миксины</h3>
						<div class="mixin-demo">
							<div class="mixin-demo__item demo-flex-center">
								.flex-center
							</div>
							<div class="mixin-demo__item demo-flex-between">
								<span>.flex-between</span>
								<span>→</span>
							</div>
						</div>
					</div>

					<div class="dev-example">
						<h3 class="h4">Адаптивная сетка</h3>
						<div class="responsive-grid-demo">
							<div class="grid-item">1</div>
							<div class="grid-item">2</div>
							<div class="grid-item">3</div>
							<div class="grid-item">4</div>
						</div>
					</div>
				</div>
			</section>

			<!-- Код примеры -->
			<section class="dev-section">
				<h2 class="h2">Примеры использования</h2>
				<div class="code-examples">
					<div class="code-example">
						<h3 class="h4">Контейнеры</h3>
						<pre class="code-block"><code>&lt;div class="container"&gt;
  &lt;!-- Контент --&gt;
&lt;/div&gt;

&lt;div class="container-narrow"&gt;
  &lt;!-- Узкий контент --&gt;
&lt;/div&gt;</code></pre>
					</div>

					<div class="code-example">
						<h3 class="h4">SCSS миксины</h3>
						<pre class="code-block"><code>.my-component {
  @include flex-center();
  @include responsive-grid(1, 2, 3);
  @include transition(opacity, 0.3s);
}</code></pre>
					</div>
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

.dev-examples {
	@include responsive-grid(1, 1, 2);
	gap: var(--spacing-xl);
	margin-top: var(--spacing-lg);
}

.dev-example {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
}

.mb-lg { margin-bottom: var(--spacing-lg); }
.mb-md { margin-bottom: var(--spacing-md); }

.demo-container {
	background: var(--color-surface);
	padding: var(--spacing-md);
	border: 1px solid var(--color-border);
}

.demo-container-center {
	background: var(--color-surface);
	border: 1px solid var(--color-border);
	height: 100px;
}

.demo-flex-center {
	@include flex-center();
	background: var(--color-primary);
	color: white;
	padding: var(--spacing-md);
	margin: var(--spacing-sm);
	height: 60px;
}

.demo-flex-between {
	@include flex-between();
	background: var(--color-secondary);
	color: white;
	padding: var(--spacing-md);
	margin: var(--spacing-sm);
	height: 60px;
}

.visibility-demo {
	display: flex;
	gap: var(--spacing-md);
	flex-wrap: wrap;
}

.visibility-item {
	padding: var(--spacing-sm) var(--spacing-md);
	background-color: var(--color-primary);
	color: white;
	border-radius: 4px;
}

.mixin-demo {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-sm);
}

.mixin-demo__item {
	border-radius: 4px;
	min-height: 40px;
}

.responsive-grid-demo {
	@include responsive-grid(1, 2, 4);
	gap: var(--spacing-md);
}

.grid-item {
	background-color: var(--color-primary);
	color: white;
	padding: var(--spacing-md);
	border-radius: 4px;
	text-align: center;
	font-weight: 500;
}

.code-examples {
	@include responsive-grid(1, 1, 2);
	gap: var(--spacing-lg);
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