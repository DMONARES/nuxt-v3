# Адаптивная система стилей

Современная, масштабируемая система стилей с полной адаптивностью и удобной архитектурой.

## 🏗️ Архитектура

```text
assets/styles/
├── index.scss              # Главный файл импорта
├── _setup.scss            # Настройки и переменные
├── variables/             # CSS переменные
│   ├── _index.scss
│   ├── _colors.scss       # Цветовая палитра
│   ├── _spacing.scss      # Адаптивные отступы
│   └── _typography.scss   # Адаптивная типографика
├── base/                  # Базовые стили
│   ├── _reset.scss        # CSS Reset
│   ├── _fonts.scss        # Подключение шрифтов
│   ├── _global.scss       # Глобальные стили
│   ├── _typography.scss   # Типографические классы
│   ├── _mixins.scss       # SCSS миксины
│   └── _helpers.scss      # Utility классы
└── examples.scss          # Примеры использования
```

## 📱 Брейкпоинты

```scss
$breakpoints: (
  xs: 0,      // Мобильные
  sm: 576px,  // Большие мобильные
  md: 768px,  // Планшеты
  lg: 992px,  // Маленькие десктопы
  xl: 1200px, // Десктопы
  xxl: 1400px // Большие десктопы
);
```

## 🎨 Использование

### Миксины для медиа-запросов

```scss
// Интуитивные названия
@include mobile() { /* до 767px */ }
@include tablet() { /* 768px - 1023px */ }
@include desktop() { /* от 1024px */ }

// "От" определенного размера
@include mobile-up() { /* от 576px */ }
@include tablet-up() { /* от 768px */ }
@include desktop-up() { /* от 1024px */ }
@include large-up() { /* от 1200px */ }
@include xlarge-up() { /* от 1400px */ }
```

### Адаптивные отступы

```scss
// Автоматически адаптивные
.element {
  padding: var(--spacing-md); // 12px → 16px → 24px
  margin: var(--spacing-lg);  // 16px → 24px → 32px
}

// С помощью миксина
.element {
  @include responsive-spacing(padding, 16px, 24px, 32px);
}
```

### Адаптивная типографика

```scss
// Fluid typography с clamp()
.title {
  font-size: var(--font-size-h1); // clamp(1.75rem, 4vw, 2.5rem)
}

// Адаптивные размеры
.text-responsive {
  font-size: var(--font-size-base); // 14px → 16px → 18px
}
```

### Адаптивная сетка

```scss
// Автоматически адаптивная сетка
.grid {
  @include responsive-grid(1, 2, 3); // 1 колонка → 2 → 3
}

// Utility классы
.grid-2 { @include responsive-grid(1, 2, 2); }
.grid-3 { @include responsive-grid(1, 2, 3); }
.grid-4 { @include responsive-grid(1, 2, 4); }
```

### Контейнеры

```scss
.container        // Центрированный, адаптивные отступы
.container-fluid  // На всю ширину
.container-narrow // Узкий (800px)
.container-center // Центрированный контент
```

### Utility классы

```scss
// Отступы
.p-md, .m-lg, .p-xl

// Размеры текста
.text-sm, .text-lg, .text-xl

// Display
.d-flex, .d-grid, .d-none

// Flex
.flex-center, .flex-between, .flex-column

// Visibility
.hidden-mobile, .visible-desktop
```

## 🎯 Примеры использования

### Адаптивная карточка

```scss
.card {
  @include responsive-spacing(padding, var(--spacing-md), var(--spacing-lg));
  background: var(--color-surface);
  border-radius: 8px;
  
  @include respond-to(md) {
    border-radius: 12px;
  }
}
```

### Адаптивная навигация

```scss
.nav {
  @include flex-between();
  @include responsive-spacing(padding, var(--spacing-md));
  
  .nav-links {
    display: none;
    @include tablet-up() {
      display: flex;
    }
  }
}
```

## 🚀 Преимущества

- ✅ **Полная адаптивность** - все элементы автоматически адаптируются
- ✅ **Fluid typography** - плавное масштабирование текста
- ✅ **Современные брейкпоинты** - актуальные размеры экранов
- ✅ **Utility-first подход** - быстрая разработка
- ✅ **Модульная архитектура** - легко расширять
- ✅ **Темная тема** - встроенная поддержка
- ✅ **Производительность** - оптимизированные стили

## 📝 Подключение

```scss
// В nuxt.config.ts
css: ['@/assets/styles/index.scss']
```

Или импортируй отдельные модули:

```scss
@use "variables/index" as *;
@use "base/mixins" as *;
```
