<template>
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

    <AppCard class="w-full md:w-1/4 relative overflow-hidden p-0 min-h-75 md:min-h-full group">
      <img
        src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?q=80&w=600&auto=format&fit=crop"
        alt="Foto Profil" loading="lazy"
        class="absolute inset-0 w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">

      <div
        class="absolute inset-0 bg-linear-to-t from-black/90 via-black/30 to-transparent transition-opacity duration-500" />

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
        <UIcon
          name="i-simple-icons-github"
          class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-brand-500 transition-colors duration-300" />
        <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">GitHub</h3>
        <p class="text-xs text-gray-500 mt-1 font-mono">@dewacahaya</p>
      </AppCard>
    </NuxtLink>

    <NuxtLink to="https://linkedin.com/in/username-kamu" target="_blank" class="block group">
      <AppCard
        class="h-full flex flex-col items-center justify-center text-center p-6 group-hover:border-blue-500 dark:group-hover:border-blue-500 group-hover:-translate-y-1 transition-all duration-300">
        <UIcon
          name="i-simple-icons-linkedin"
          class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-blue-500 transition-colors duration-300" />
        <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">LinkedIn</h3>
        <p class="text-xs text-gray-500 mt-1 font-mono">Connect</p>
      </AppCard>
    </NuxtLink>

    <NuxtLink to="https://instagram.com/dewacahaya._" target="_blank" class="block group">
      <AppCard
        class="h-full flex flex-col items-center justify-center text-center p-6 group-hover:border-pink-500 dark:group-hover:border-pink-500 group-hover:-translate-y-1 transition-all duration-300">
        <UIcon
          name="i-simple-icons-instagram"
          class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-pink-500 transition-colors duration-300" />
        <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">Instagram</h3>
        <p class="text-xs text-gray-500 mt-1 font-mono">@dewacahaya._</p>
      </AppCard>
    </NuxtLink>

    <NuxtLink to="mailto:dewacahaya30@gmail.com" class="block group">
      <AppCard
        class="h-full flex flex-col items-center justify-center text-center p-6 group-hover:border-brand-500 dark:group-hover:border-brand-500 group-hover:-translate-y-1 transition-all duration-300">
        <UIcon
          name="i-heroicons-envelope"
          class="w-10 h-10 mb-3 text-gray-600 dark:text-gray-400 group-hover:text-brand-500 transition-colors duration-300" />
        <h3 class="font-bold text-gray-900 dark:text-white transition-colors duration-500">Email</h3>
        <p class="text-xs text-gray-500 mt-1 font-mono">Hire Me</p>
      </AppCard>
    </NuxtLink>
  </div>
</template>
