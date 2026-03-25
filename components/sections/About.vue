<template>
  <!-- ABOUT -->
  <section id="about" class="w-full mb-18 scroll-mt-18">
    <div class="flex flex-col lg:flex-row gap-10">
      <div class="w-full lg:w-1/2 flex flex-col gap-4">
        <AppCard
          class="relative p-0 overflow-hidden min-h-62.5 md:min-h-75 group border-0 ring-1 ring-gray-200 dark:ring-gray-800">
          <img
            src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b?q=80&w=800&auto=format&fit=crop"
            alt="Tech Abstract"
            class="absolute inset-0 w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
          <div
            class="absolute inset-0 bg-linear-to-tr from-surface-darker/80 to-transparent transition-opacity duration-500" />

          <div class="absolute bottom-6 left-6 z-10">
            <UIcon name="i-heroicons-cpu-chip" class="w-12 h-12 text-white/50" />
          </div>
        </AppCard>

        <div class="grid grid-cols-2 gap-4">
          <AppCard
            class="flex flex-col items-center justify-center text-center p-8 bg-brand-50/50 dark:bg-brand-900/10 border-0 ring-1 ring-brand-100 dark:ring-brand-900/30 hover:-translate-y-1 transition-all duration-300">
            <UIcon name="i-heroicons-code-bracket" class="w-10 h-10 text-brand-500 mb-3" />
            <h4 class="font-bold text-gray-900 dark:text-white text-lg transition-colors duration-500">Clean Code</h4>
            <p class="text-sm text-gray-500 mt-1">Advocate</p>
          </AppCard>

          <AppCard
            class="flex flex-col items-center justify-center text-center p-8 bg-purple-50/50 dark:bg-purple-900/10 border-0 ring-1 ring-purple-100 dark:ring-purple-900/30 hover:-translate-y-1 transition-all duration-300">
            <UIcon name="i-heroicons-paint-brush" class="w-10 h-10 text-purple-500 mb-3" />
            <h4 class="font-bold text-gray-900 dark:text-white text-lg transition-colors duration-500">Design</h4>
            <p class="text-sm text-gray-500 mt-1">Enthusiast</p>
          </AppCard>
        </div>
      </div>

      <div class="w-full lg:w-1/2 flex flex-col justify-center">

        <div
          class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-cyan-50 dark:bg-cyan-500/10 text-cyan-600 dark:text-cyan-400 w-fit mb-6 text-sm font-semibold border border-cyan-200 dark:border-cyan-800/30 transition-colors duration-500">
          <UIcon name="i-heroicons-sparkles" class="w-4 h-4" />
          <span>About Me</span>
        </div>

        <h2
          class="text-4xl md:text-5xl font-extrabold text-gray-900 dark:text-white leading-tight mb-6 transition-colors duration-500">
          Membangun web, <br>
          <span class="text-brand-500">satu baris kode</span> setiap saat.
        </h2>

        <div class="space-y-4 mb-8 text-lg text-gray-600 dark:text-gray-300 transition-colors duration-500">
          <p>
            Sebagai mahasiswa Teknik Informatika, saya menjembatani celah antara <b>desain antarmuka</b> dan <b>logika
              pemrograman</b>. Fokus saya adalah menciptakan pengalaman digital yang tidak hanya estetik secara
            visual, tapi juga berkinerja tinggi.
          </p>
        </div>

        <AppButton to="/about" class="w-fit mt-2 mb-8">
          Lihat Profil Lengkap & CV
        </AppButton>

        <div class="flex flex-wrap gap-2">
          <AppChip label="Problem Solver" />
          <AppChip label="Team Player" />
          <AppChip label="Fast Learner" />
          <AppChip label="Detail-Oriented" />
        </div>

      </div>
    </div>
  </section>
</template>
