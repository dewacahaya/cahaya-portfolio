<script setup>
defineProps({
  label: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    default: ''
  }
})
</script>

<template>
  <div
    class="inline-flex items-center gap-1.5 px-3 py-1.5 rounded-full border border-gray-200 dark:border-gray-800 bg-gray-50 dark:bg-surface-dark text-sm font-medium text-gray-700 dark:text-gray-300 w-fit hover:border-brand-500 hover:text-brand-500 dark:hover:border-brand-500 dark:hover:text-brand-400 transition-colors cursor-default">
    <UIcon v-if="icon" :name="icon" class="w-4 h-4 shrink-0" />
    <span>{{ label }}</span>
  </div>
</template>
