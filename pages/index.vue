<script setup lang="ts">
// Nanti ini akan diganti dengan: const { data: projects } = await useFetch('/api/projects') atau composable Firebase kamu.
const projects = [
  {
    id: 1,
    title: 'Sistem Informasi Ormawa INSTIKI',
    category: 'Web System',
    description: 'Platform web terintegrasi yang dirancang khusus untuk mengelola data, kegiatan, dan administrasi organisasi mahasiswa di lingkungan kampus secara terpusat.',
    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?q=80&w=800&auto=format&fit=crop',
    link: '#', // Link ke source code / web
    tech: [
      { name: 'Vue.js', icon: 'i-logos-vue' },
      { name: 'Tailwind', icon: 'i-logos-tailwindcss-icon' },
      { name: 'PHP', icon: 'i-logos-php' }
    ]
  },
  {
    id: 2,
    title: 'AI Tourism Chatbot Bali',
    category: 'AI / Chatbot',
    description: 'Asisten virtual pintar berbasis kecerdasan buatan untuk melayani pertanyaan tamu dan memberikan rekomendasi wisata secara real-time pada hotel bintang 5.',
    image: 'https://images.unsplash.com/photo-1592595896616-c37162298647?q=80&w=800&auto=format&fit=crop',
    link: '#',
    tech: [
      { name: 'Nuxt 3', icon: 'i-logos-nuxt-icon' },
      { name: 'Python', icon: 'i-logos-python' },
      { name: 'OpenAI', icon: 'i-simple-icons-openai' }
    ]
  },
  {
    id: 3,
    title: 'Manga Reader App',
    category: 'Mobile App',
    description: 'Aplikasi pembaca komik lintas platform dengan fitur bookmark, unduhan offline, dan transisi halaman yang dioptimalkan untuk perangkat layar sentuh.',
    image: 'https://images.unsplash.com/photo-1613324684888-251f2f012019?q=80&w=800&auto=format&fit=crop',
    link: '#',
    tech: [
      { name: 'Flutter', icon: 'i-logos-flutter' },
      { name: 'Firebase', icon: 'i-logos-firebase' }
    ]
  },
  {
    id: 4,
    title: 'E-Commerce Dashboard',
    category: 'UI/UX Design',
    description: 'Eksplorasi desain antarmuka untuk panel admin toko online yang menonjolkan visualisasi data penjualan dan kemudahan manajemen inventaris barang.',
    image: 'https://images.unsplash.com/photo-1460925895917-afdab827c52f?q=80&w=800&auto=format&fit=crop',
    link: '#',
    tech: [
      { name: 'Figma', icon: 'i-logos-figma' }
    ]
  }
]
</script>

<template>
  <main class="w-full max-w-7xl mx-auto flex flex-col gap-10 mt-8 px-4 md:px-6 transition-colors duration-500">

    <!-- HERO SECTION -->
    <div class="flex flex-col md:flex-row gap-6 w-full h-auto md:h-100">
      <div
        class="inline-flex sm:hidden items-center gap-2 px-4 py-2 rounded-full border border-brand-500/30 bg-brand-50 dark:bg-brand-500/10 w-fit transition-colors duration-500">
        <span class="relative flex h-3 w-3">
          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-brand-400 opacity-75" />
          <span class="relative inline-flex rounded-full h-3 w-3 bg-brand-500" />
        </span>
        <span class="text-sm font-semibold text-brand-600 dark:text-brand-400">
          Available!
        </span>
      </div>

      <AppCard class="w-full hidden md:flex p-8 md:w-3/4 flex-col justify-center h-full group">
        <div
          class="inline-flex items-center gap-2 px-4 py-2 rounded-full border border-brand-500/30 bg-brand-50 dark:bg-brand-500/10 w-fit mb-6 transition-colors duration-500">
          <span class="relative flex h-3 w-3">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-brand-400 opacity-75" />
            <span class="relative inline-flex rounded-full h-3 w-3 bg-brand-500" />
          </span>
          <span class="text-sm font-semibold text-brand-600 dark:text-brand-400">
            Available!
          </span>
        </div>

        <h1
          class="text-4xl md:text-6xl font-bold text-gray-900 dark:text-white leading-tight tracking-tight transition-colors duration-500">
          Membangun web yang <br class="hidden md:block">
          <span class="text-brand-500">cepat & interaktif.</span>
        </h1>

        <p
          class="mt-4 text-lg md:text-xl text-gray-600 dark:text-gray-300 max-w-2xl leading-relaxed transition-colors duration-500">
          Saya mengkhususkan diri dalam pengembangan antarmuka modern yang berfokus pada pengalaman pengguna yang
          optimal.
        </p>
      </AppCard>

      <AppCard class="w-full md:w-1/4 relative overflow-hidden p-0 min-h-[300px] md:min-h-full group">
        <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?q=80&w=600&auto=format&fit=crop"
          alt="Foto Profil"
          class="absolute inset-0 w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">

        <div
          class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/30 to-transparent transition-opacity duration-500" />

        <div class="absolute inset-0 p-6 flex flex-col justify-end z-10">
          <p class="text-white font-bold text-xl leading-snug">
            Dewa Cahaya
          </p>
          <p class="text-gray-300 text-sm flex items-center gap-1 mt-2">
            <UIcon name="i-heroicons-map-pin" class="w-4 h-4 text-brand-400" />
            Bali, Indonesia
          </p>
        </div>
      </AppCard>
    </div>

    <!-- SOCIAL MEDIA -->
    <div class="grid grid-cols-2 md:grid-cols-4 gap-6 w-full">
      <NuxtLink to="https://github.com/dewacahaya" target="_blank" class="block group">
        <AppCard
          class="h-full flex flex-col items-center justify-center text-center p-6 group-hover:border-brand-500 dark:group-hover:border-brand-500 group-hover:-translate-y-1 transition-all duration-300">
          <UIcon name="i-simple-icons-github"
            class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-brand-500 transition-colors duration-300" />
          <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">GitHub</h3>
          <p class="text-xs text-gray-500 mt-1 font-mono">@dewacahaya</p>
        </AppCard>
      </NuxtLink>

      <NuxtLink to="https://linkedin.com/in/username-kamu" target="_blank" class="block group">
        <AppCard
          class="h-full flex flex-col items-center justify-center text-center p-6 group-hover:border-blue-500 dark:group-hover:border-blue-500 group-hover:-translate-y-1 transition-all duration-300">
          <UIcon name="i-simple-icons-linkedin"
            class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-blue-500 transition-colors duration-300" />
          <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">LinkedIn</h3>
          <p class="text-xs text-gray-500 mt-1 font-mono">Connect</p>
        </AppCard>
      </NuxtLink>

      <NuxtLink to="https://instagram.com/dewacahaya._" target="_blank" class="block group">
        <AppCard
          class="h-full flex flex-col items-center justify-center text-center p-6 group-hover:border-pink-500 dark:group-hover:border-pink-500 group-hover:-translate-y-1 transition-all duration-300">
          <UIcon name="i-simple-icons-instagram"
            class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-pink-500 transition-colors duration-300" />
          <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">Instagram</h3>
          <p class="text-xs text-gray-500 mt-1 font-mono">@dewacahaya._</p>
        </AppCard>
      </NuxtLink>

      <NuxtLink to="mailto:dewacahaya30@gmail.com" class="block group">
        <AppCard
          class="h-full flex flex-col items-center justify-center text-center p-6 group-hover:border-brand-500 dark:group-hover:border-brand-500 group-hover:-translate-y-1 transition-all duration-300">
          <UIcon name="i-heroicons-envelope"
            class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-brand-500 transition-colors duration-300" />
          <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">Email</h3>
          <p class="text-xs text-gray-500 mt-1 font-mono">Hire Me</p>
        </AppCard>
      </NuxtLink>
    </div>

    <!-- MARQUEE -->
    <AppMarquee />

    <!-- ABOUT -->
    <section id="about" class="w-full mb-18 scroll-mt-18">
      <div class="flex flex-col lg:flex-row gap-10">
        <div class="w-full lg:w-1/2 flex flex-col gap-4">
          <AppCard
            class="relative p-0 overflow-hidden min-h-[250px] md:min-h-[300px] group border-0 ring-1 ring-gray-200 dark:ring-gray-800">
            <img src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b?q=80&w=800&auto=format&fit=crop"
              alt="Tech Abstract"
              class="absolute inset-0 w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
            <div
              class="absolute inset-0 bg-gradient-to-tr from-surface-darker/80 to-transparent transition-opacity duration-500">
            </div>

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

    <!-- PROJECTS -->
    <section id="projects" class="w-full max-w-7xl mb-18 mx-auto scroll-mt-6">
      <div class="w-full mb-10">
        <div
          class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-orange-50 dark:bg-orange-500/10 text-orange-600 dark:text-orange-400 w-fit mb-4 text-sm font-semibold border border-orange-200 dark:border-orange-800/30 transition-colors duration-500">
          <UIcon name="i-heroicons-briefcase" class="w-4 h-4" />
          <span>PORTFOLIO</span>
        </div>

        <h2
          class="text-4xl md:text-5xl font-extrabold text-gray-900 dark:text-white leading-tight transition-colors duration-500">
          Featured
          <span class="bg-linear-to-br from-indigo-600 to-blue-500 bg-clip-text text-transparent">
            Projects
          </span>
        </h2>
      </div>

      <UCarousel v-slot="{ item }" :items="projects" :ui="{ item: 'basis-full md:basis-1/2 lg:basis-1/3 snap-start' }"
        class="w-full -ml-4" arrows indicators>
        <div class="pl-4 pb-12 h-full w-full flex">

          <AppCard
            class="p-0 overflow-hidden group flex flex-col border border-gray-200 dark:border-gray-800 transition-all duration-500 hover:-translate-y-2 hover:shadow-xl hover:shadow-brand-500/10 h-full w-full cursor-pointer">

            <div class="relative w-full h-48 overflow-hidden bg-gray-100 dark:bg-surface-darker shrink-0">
              <img :src="item.image" :alt="item.title"
                class="absolute inset-0 w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">

              <div
                class="absolute top-4 left-4 bg-white/90 dark:bg-surface-darker/90 backdrop-blur-sm px-3 py-1.5 rounded-lg text-xs font-bold text-gray-800 dark:text-white shadow-sm transition-colors duration-500">
                {{ item.category }}
              </div>

              <NuxtLink :to="item.link" target="_blank"
                class="absolute top-4 right-4 bg-black/60 hover:bg-brand-500 backdrop-blur-md p-2 rounded-full text-white opacity-0 translate-y-4 group-hover:opacity-100 group-hover:translate-y-0 transition-all duration-300 z-10 shadow-lg">
                <UIcon name="i-heroicons-arrow-up-right" />
              </NuxtLink>
            </div>

            <div
              class="p-6 flex flex-col grow justify-between bg-white dark:bg-surface-dark transition-colors duration-500">

              <div>
                <h3
                  class="text-xl font-bold text-gray-900 dark:text-white mb-3 transition-colors duration-500 group-hover:text-brand-500 line-clamp-2">
                  {{ item.title }}
                </h3>
                <p
                  class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed transition-colors duration-500 line-clamp-3">
                  {{ item.description }}
                </p>
              </div>

              <div class="mt-6 flex flex-wrap gap-2">
                <AppChip v-for="tech in item.tech" :key="tech.name" :label="tech.name" :icon="tech.icon" />
              </div>
            </div>
          </AppCard>
        </div>
      </UCarousel>
    </section>

    <!-- EXPERIENCES -->
    <section id="experience">
      halo
    </section>

  </main>
</template>
