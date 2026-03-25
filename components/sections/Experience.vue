<script lang="ts" setup>
const experiences = [
  {
    id: 1,
    title: 'Lead Front-End Developer',
    organization: 'Project Sistem Informasi Ormawa',
    date: '2025 - Present',
    location: 'Bali, ID (Hybrid)',
    description: 'Memimpin pengembangan antarmuka (UI/UX) dan implementasi frontend menggunakan Vue.js dan Tailwind CSS untuk platform manajemen organisasi mahasiswa di INSTIKI.',
    icon: 'i-heroicons-computer-desktop'
  },
  {
    id: 2,
    title: 'Anggota Divisi Ristek (Riset & Teknologi)',
    organization: 'Himpunan Mahasiswa Teknik Informatika',
    date: '2024 - 2025',
    location: 'Denpasar, Bali',
    description: 'Aktif dalam penyelenggaraan workshop teknologi, pengenalan bahasa pemrograman baru, serta mengelola website internal himpunan kampus.',
    icon: 'i-heroicons-user-group'
  },
  {
    id: 3,
    title: 'Mahasiswa Teknik Informatika',
    organization: 'Institut Bisnis dan Teknologi Indonesia (INSTIKI)',
    date: '2023 - Present',
    location: 'Bali, ID',
    description: 'Fokus pada pengembangan perangkat lunak, sistem basis data, dan kecerdasan buatan (AI). Aktif mengeksplorasi web development secara otodidak.',
    icon: 'i-heroicons-academic-cap'
  }
]
</script>
<template>
  <!-- EXPERIENCES -->
  <section id="experience" class="w-full max-w-7xl mb-18 mx-auto scroll-mt-8 px-4 md:px-6">

    <div class="w-full mb-12 text-center">
      <div
        class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-cyan-50 dark:bg-cyan-500/10 text-cyan-600 dark:text-cyan-400 w-fit mb-4 text-sm font-semibold border border-cyan-200 dark:border-cyan-800/30 transition-colors duration-500">
        <UIcon name="i-heroicons-briefcase" class="w-4 h-4" />
        <span>CAREER PATH</span>
      </div>

      <h2
        class="text-4xl md:text-5xl font-extrabold text-gray-900 dark:text-white leading-tight transition-colors duration-500">
        My
        <span class="bg-linear-to-br from-indigo-600 to-blue-500 bg-clip-text text-transparent">
          Journey
        </span>
      </h2>
      <p class="pt-4 text-gray-600 dark:text-gray-400 transition-colors duration-500 max-w-2xl mx-auto">
        My experience in studying, committees, volunteering, and project work.
      </p>
    </div>

    <div class="relative w-full">
      <div
        class="hidden md:block absolute left-2.75 md:left-3.75 top-8 bottom-0 w-0.5 bg-gray-200 dark:bg-gray-800 transition-colors duration-500" />

      <div class="flex flex-col gap-6 md:gap-8 w-full">

        <div v-for="(exp) in experiences" :key="exp.id" class="relative pl-0 md:pl-14 group">

          <div
            class="hidden md:block absolute left-0 md:left-1 top-6 w-6 h-6 rounded-full border-4 border-surface-light dark:border-surface-darker bg-cyan-500 z-10 transition-transform duration-300 group-hover:scale-125" />

          <AppCard
            class="p-5 md:p-8 hover:-translate-y-1 hover:shadow-xl hover:shadow-indigo-500/10 transition-all duration-300 border border-gray-100 dark:border-gray-500 bg-white dark:bg-surface-dark">

            <div class="flex flex-col sm:flex-row gap-4 sm:gap-6">

              <div class="flex items-center sm:items-start gap-4 shrink-0">
                <div
                  class="w-12 h-12 sm:w-14 sm:h-14 shrink-0 rounded-2xl bg-indigo-50 dark:bg-indigo-500/10 flex items-center justify-center border border-indigo-100 dark:border-indigo-500/20 transition-colors duration-500">
                  <UIcon :name="exp.icon" class="w-6 h-6 sm:w-7 sm:h-7 text-indigo-500" />
                </div>

                <div class="flex flex-col sm:hidden">
                  <h3
                    class="text-lg font-bold text-gray-900 dark:text-white transition-colors duration-500 group-hover:text-indigo-500 leading-tight">
                    {{ exp.title }}
                  </h3>
                  <p class="text-sm font-medium text-gray-800 dark:text-gray-200 mt-0.5 transition-colors duration-500">
                    {{ exp.organization }}
                  </p>
                </div>
              </div>

              <div class="flex flex-col w-full">
                <div class="hidden sm:block">
                  <h3
                    class="text-xl font-bold text-gray-900 dark:text-white transition-colors duration-500 group-hover:text-indigo-500">
                    {{ exp.title }}
                  </h3>
                  <p class="text-md font-medium text-gray-800 dark:text-gray-200 mt-1 transition-colors duration-500">
                    {{ exp.organization }}
                  </p>
                </div>

                <div
                  class="flex flex-wrap items-center gap-x-4 gap-y-2 mt-2 sm:mt-3 text-sm text-gray-500 dark:text-gray-400 transition-colors duration-500">
                  <span class="flex items-center gap-1.5">
                    <UIcon name="i-heroicons-calendar" class="w-4 h-4 shrink-0" />
                    {{ exp.date }}
                  </span>
                  <span class="hidden sm:inline-block text-gray-300 dark:text-gray-600">&bull;</span>
                  <span class="flex items-center gap-1.5">
                    <UIcon name="i-heroicons-map-pin" class="w-4 h-4 shrink-0" />
                    {{ exp.location }}
                  </span>
                </div>

                <p
                  class="mt-3 sm:mt-4 text-sm sm:text-base text-gray-600 dark:text-gray-300 leading-relaxed transition-colors duration-500">
                  {{ exp.description }}
                </p>
              </div>

            </div>

          </AppCard>
        </div>
      </div>

    </div>
  </section>
</template>
