<script lang="ts" setup>
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
</template>
