<script setup>
// Демонстрация UI компонентов
definePageMeta({
  title: 'Design System - UI Компоненты'
})

// Реактивные переменные для демонстрации
const inputValue = ref('')
const emailValue = ref('')
const errorValue = ref('')
const disabledValue = ref('Заблокировано')
const phoneValue = ref('')

const checkbox1 = ref(false)
const checkbox2 = ref(true)
const checkbox3 = ref(false)

const regName = ref('')
const regEmail = ref('')
const regPhone = ref('')
const regAgree = ref(false)
</script>

<template>
	<DevPage
		title="UI Компоненты"
		description="Готовые компоненты интерфейса для быстрой разработки"
	>

			<!-- Кнопки -->
			<section class="dev-section">
				<h2 class="h2">Кнопки</h2>
				<p class="text-p text-secondary mb-lg">
					Различные варианты кнопок для действий пользователя
				</p>

				<div class="component-examples">
					<div class="component-example">
						<h3 class="h4">Основные кнопки</h3>
						<div class="button-group">
							<UiButton>Обычная кнопка</UiButton>
							<UiButton variant="border">Кнопка с рамкой</UiButton>
							<UiButton disabled>Отключенная кнопка</UiButton>
						</div>
					</div>

					<div class="component-example">
						<h3 class="h4">Размеры кнопок</h3>
						<div class="button-group">
							<UiButton>Обычный размер</UiButton>
							<UiButton size="xl">Большой размер</UiButton>
						</div>
					</div>
				</div>
			</section>

			<!-- Поля ввода -->
			<section class="dev-section">
				<h2 class="h2">Поля ввода</h2>
				<p class="text-p text-secondary mb-lg">
					Формы и поля для ввода данных
				</p>

				<div class="component-examples">
					<div class="component-example">
						<h3 class="h4">Базовые поля</h3>
						<div class="form-group">
							<UiInput
								v-model="inputValue"
								label="Имя пользователя"
								placeholder="Введите имя"
							/>
							<UiInput
								v-model="emailValue"
								type="email"
								label="Email"
								placeholder="example@email.com"
							/>
						</div>
					</div>

					<div class="component-example">
						<h3 class="h4">Состояния полей</h3>
						<div class="form-group">
							<UiInput
								v-model="errorValue"
								label="Поле с ошибкой"
								placeholder="Введите данные"
								:error="true"
								error-text="Это поле обязательно для заполнения"
							/>
							<UiInput
								v-model="disabledValue"
								label="Отключенное поле"
								placeholder="Недоступно"
								:disabled="true"
							/>
						</div>
					</div>

					<div class="component-example">
						<h3 class="h4">Телефон</h3>
						<div class="form-group">
							<UiInput
								v-model="phoneValue"
								label="Номер телефона"
								placeholder="+7 (999) 999-99-99"
								:is-phone="true"
							/>
						</div>
					</div>
				</div>
			</section>

			<!-- Чекбоксы -->
			<section class="dev-section">
				<h2 class="h2">Чекбоксы</h2>
				<p class="text-p text-secondary mb-lg">
					Элементы для выбора опций
				</p>

				<div class="component-examples">
					<div class="component-example">
						<h3 class="h4">Базовые чекбоксы</h3>
						<div class="checkbox-group">
							<UiCheckbox v-model="checkbox1" label="Согласен с условиями" />
							<UiCheckbox v-model="checkbox2" label="Подписаться на рассылку" />
							<UiCheckbox v-model="checkbox3" label="Отключенный чекбокс" :disabled="true" />
						</div>
					</div>
				</div>
			</section>

			<!-- Аккордеон -->
			<section class="dev-section">
				<h2 class="h2">Аккордеон</h2>
				<p class="text-p text-secondary mb-lg">
					Сворачиваемые секции контента
				</p>

				<div class="component-examples">
					<div class="component-example">
						<h3 class="h4">Базовый аккордеон</h3>
						<div class="accordion-group">
							<UiAccordion title="Как начать работу?">
								<p class="text-p">
									Для начала работы с системой необходимо зарегистрироваться, 
									заполнив форму регистрации на главной странице.
								</p>
							</UiAccordion>
							<UiAccordion title="Какие функции доступны?">
								<p class="text-p">
									В системе доступны следующие функции: создание проектов, 
									управление задачами, командная работа и аналитика.
								</p>
							</UiAccordion>
							<UiAccordion title="Как получить поддержку?">
								<p class="text-p">
									Для получения поддержки обратитесь к нашей команде через 
									форму обратной связи или по email support@example.com
								</p>
							</UiAccordion>
						</div>
					</div>
				</div>
			</section>

			<!-- Скелетоны -->
			<section class="dev-section">
				<h2 class="h2">Скелетоны</h2>
				<p class="text-p text-secondary mb-lg">
					Заглушки для загрузки контента
				</p>

				<div class="component-examples">
					<div class="component-example">
						<h3 class="h4">Загрузка контента</h3>
						<div class="skeleton-examples">
							<UiSkeleton height="20px" width="200px" />
							<UiSkeleton height="16px" width="150px" />
							<UiSkeleton height="100px" width="100%" />
						</div>
					</div>

					<div class="component-example">
						<h3 class="h4">Карточка товара</h3>
						<div class="skeleton-card">
							<UiSkeleton height="200px" width="100%" />
							<div class="skeleton-content">
								<UiSkeleton height="24px" width="80%" />
								<UiSkeleton height="16px" width="60%" />
								<UiSkeleton height="32px" width="120px" />
							</div>
						</div>
					</div>
				</div>
			</section>

			<!-- Примеры использования -->
			<section class="dev-section">
				<h2 class="h2">Примеры использования</h2>
				<div class="usage-examples">
					<div class="usage-example">
						<h3 class="h4">Форма регистрации</h3>
						<div class="registration-form">
							<h4 class="h4">Регистрация</h4>
							<div class="form-group">
								<UiInput
									v-model="regName"
									label="Имя"
									placeholder="Введите ваше имя"
								/>
								<UiInput
									v-model="regEmail"
									type="email"
									label="Email"
									placeholder="example@email.com"
								/>
								<UiInput
									v-model="regPhone"
									label="Телефон"
									placeholder="+7 (999) 999-99-99"
									:is-phone="true"
								/>
								<UiCheckbox v-model="regAgree" label="Согласен с условиями использования" />
								<UiButton size="xl" class="w-full">Зарегистрироваться</UiButton>
							</div>
						</div>
					</div>

					<div class="usage-example">
						<h3 class="h4">Карточка продукта</h3>
						<div class="product-card">
							<div class="product-image">
								<UiSkeleton height="200px" width="100%" />
							</div>
							<div class="product-info">
								<h4 class="h4">Название продукта</h4>
								<p class="text-p text-secondary">Описание продукта</p>
								<div class="product-price">
									<span class="h5 text-primary">1 299 ₽</span>
								</div>
								<div class="product-actions">
									<UiButton>В корзину</UiButton>
									<UiButton variant="border">Подробнее</UiButton>
								</div>
							</div>
						</div>
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

.component-examples {
	@include responsive-grid(1, 1, 2);
	gap: var(--spacing-xl);
	margin-top: var(--spacing-lg);
}

.component-example {
	background-color: var(--color-surface);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
}

.button-group {
	display: flex;
	flex-wrap: wrap;
	gap: var(--spacing-md);
	margin-top: var(--spacing-md);
}

.form-group {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-lg);
	margin-top: var(--spacing-md);
}

.checkbox-group {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-md);
	margin-top: var(--spacing-md);
}

.accordion-group {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-sm);
	margin-top: var(--spacing-md);
}

.skeleton-examples {
	display: flex;
	flex-direction: column;
	gap: var(--spacing-md);
	margin-top: var(--spacing-md);
}

.skeleton-card {
	background-color: var(--color-background);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	overflow: hidden;
	margin-top: var(--spacing-md);
}

.skeleton-content {
	padding: var(--spacing-lg);
	display: flex;
	flex-direction: column;
	gap: var(--spacing-md);
}

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

.registration-form {
	background-color: var(--color-background);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	padding: var(--spacing-lg);
	margin-top: var(--spacing-md);
}

.product-card {
	background-color: var(--color-background);
	border: 1px solid var(--color-border);
	border-radius: 8px;
	overflow: hidden;
	margin-top: var(--spacing-md);
}

.product-image {
	width: 100%;
}

.product-info {
	padding: var(--spacing-lg);
}

.product-price {
	margin: var(--spacing-md) 0;
}

.product-actions {
	display: flex;
	gap: var(--spacing-md);
	margin-top: var(--spacing-lg);
}

.w-full {
	width: 100%;
}

.mb-lg { margin-bottom: var(--spacing-lg); }
</style>