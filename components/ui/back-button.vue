<script setup>
const router = useRouter()

const goBack = () => {
  router.back()
}
</script>

<template>
  <button @click="goBack" class="back-button">
    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
      <path d="M20 11H7.83l5.59-5.59L12 4l-8 8 8 8 1.41-1.41L7.83 13H20v-2z"/>
    </svg>
    Назад
  </button>
</template>

<style lang="scss" scoped>
@use "~/assets/styles/variables/index" as *;

.back-button {
  display: inline-flex;
  align-items: center;
  gap: var(--spacing-sm);
  padding: var(--spacing-sm) var(--spacing-md);
  background-color: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: 6px;
  color: var(--color-text);
  font-size: 0.875rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;

  &:hover {
    background-color: var(--color-primary);
    color: white;
    border-color: var(--color-primary);
  }

  &:active {
    transform: translateY(1px);
  }
}
</style>
