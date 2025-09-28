<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="dev-page">
    <div class="container">
      <div class="dev-header">
        <div class="dev-header__top">
          <UiBackButton />
        </div>
        <h1 class="h1">{{ title }}</h1>
        <p class="text-p text-secondary">
          {{ description }}
        </p>
      </div>
      <slot />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "~/assets/styles/variables/index" as *;

.dev-page {
  min-height: 100vh;
  background-color: var(--color-background);
  padding: var(--spacing-xxl) 0;
}

.dev-header {
  margin-bottom: var(--spacing-xxl);
}

.dev-header__top {
  margin-bottom: var(--spacing-lg);
}
</style>
