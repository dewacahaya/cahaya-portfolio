<script setup>

</script>

<template>
  <!-- CONTACT -->
  <section class="w-full max-w-5xl mx-auto mb-24 px-4 md:px-6">
    <div
      class="relative overflow-hidden rounded-3xl border border-gray-200 dark:border-gray-500 bg-white dark:bg-surface-dark transition-colors duration-500 shadow-sm group">

      <div
        class="absolute inset-0 bg-linear-to-br from-indigo-500/5 via-transparent to-fuchsia-500/5 pointer-events-none" />

      <div class="relative p-10 md:p-16 flex flex-col items-center text-center">

        <div
          class="w-14 h-14 rounded-full bg-linear-to-br from-blue-600 to-fuchsia-500 flex items-center justify-center mb-8 shadow-lg shadow-fuchsia-500/20 group-hover:scale-110 transition-transform duration-500">
          <UIcon name="i-heroicons-sparkles-solid" class="w-7 h-7 text-white" />
        </div>

        <h2
          class="text-4xl md:text-5xl font-extrabold text-gray-900 dark:text-white leading-tight mb-4 transition-colors duration-500">
          Interested to discuss <br class="hidden md:block">
          <span class="bg-linear-to-r from-blue-600 to-fuchsia-500 bg-clip-text text-transparent">some topic?</span>
        </h2>

        <p
          class="text-gray-600 dark:text-gray-300 max-w-2xl text-lg mb-10 leading-relaxed transition-colors duration-500">
          Thank you for scrolling this far! If you're looking for a developer who cares about the details, let's
          connect and build something amazing together.
        </p>

        <div class="flex flex-col sm:flex-row items-center gap-4 mb-10">
          <UButton to="mailto:dewacahaya30@gmail.com" label="Let's Connect" icon="i-heroicons-arrow-right" trailing
            size="xl"
            class="rounded-full px-8 py-3 bg-gray-900 text-white hover:bg-gray-800 dark:bg-white dark:text-gray-900 dark:hover:bg-gray-100 transition-colors" />
          <UButton to="/about" label="View Resume" icon="i-heroicons-paper-airplane" color="neutral" variant="soft"
            size="xl"
            class="rounded-full px-8 py-3 bg-gray-100 hover:bg-gray-200 dark:bg-surface-darker dark:hover:bg-gray-800 transition-colors" />
        </div>

        <div
          class="flex flex-col md:flex-row items-center gap-3 text-sm font-medium text-gray-500 dark:text-gray-400 transition-colors duration-500">
          <div class="flex items-center gap-2">
            <span class="relative flex h-2.5 w-2.5">
              <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75" />
              <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-emerald-500" />
            </span>
            Available for work
          </div>
          <span class="w-1 h-1 rounded-full bg-gray-300 dark:bg-gray-700" />
          <div>Usually responds in 24h</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
