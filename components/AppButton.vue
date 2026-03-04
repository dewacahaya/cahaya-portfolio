<script setup>
defineProps({
  // Prop untuk link tujuan (misal: '/about')
  to: {
    type: String,
    default: ''
  },
  // Prop untuk ikon opsional (bisa diganti jika perlu)
  icon: {
    type: String,
    default: 'i-heroicons-arrow-long-right-20-solid'
  }
})
</script>

<template>
  <NuxtLink :to="to"
    class="group relative inline-flex items-center justify-center gap-2 px-6 py-3 font-semibold rounded-full overflow-hidden transition-all duration-300 ring-1 ring-brand-500/30 bg-brand-50/50 dark:bg-brand-500/10 text-brand-600 dark:text-brand-400 hover:ring-brand-500 hover:shadow-lg hover:shadow-brand-500/20">
    <span
      class="absolute inset-0 w-full h-full bg-brand-100 dark:bg-brand-500/20 transform scale-x-0 group-hover:scale-x-100 transition-transform duration-300 origin-left" />

    <span class="relative flex items-center gap-2">
      <slot />

      <UIcon :name="icon" class="w-5 h-5 transition-transform duration-300 group-hover:translate-x-1.5" />
    </span>
  </NuxtLink>
</template>
