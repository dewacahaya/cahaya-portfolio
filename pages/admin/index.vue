<script setup>
// INI KUNCINYA 🔑
definePageMeta({
  layout: 'admin'
  // middleware: 'auth' (Nanti kita aktifkan ini untuk proteksi)
})
</script>

<template>
  <div>
    <h1 class="text-3xl font-bold text-gray-800 dark:text-white">
      Dashboard Overview
    </h1>
    <p class="mt-4 text-gray-600 dark:text-gray-300">
      Selamat datang di panel admin portofoliomu.
    </p>

    <div class="grid grid-cols-3 gap-4 mt-8">
      <div class="p-6 bg-white dark:bg-surface-dark rounded-xl shadow-sm border border-gray-200 dark:border-gray-700">
        <h3 class="text-lg font-semibold">
          Total Projects
        </h3>
        <p class="text-4xl font-bold text-brand-500 mt-2">
          12
        </p>
      </div>
    </div>
  </div>
</template>
