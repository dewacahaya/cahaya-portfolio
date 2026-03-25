<template>
  <footer
    class="w-full border-t border-gray-200 dark:border-gray-800 bg-white dark:bg-surface-darker transition-colors duration-500 pt-16 pb-8">
    <div class="max-w-7xl mx-auto px-4 md:px-6">

      <div class="grid grid-cols-1 md:grid-cols-12 gap-10 md:gap-6 mb-16">

        <div class="md:col-span-12 lg:col-span-5">
          <NuxtLink to="/" class="text-2xl font-bold font-sans text-brand-500 tracking-tighter inline-block mb-4">
            MY <span class="text-gray-900 dark:text-white transition-colors duration-500">PORTFOLIO</span>.
          </NuxtLink>
          <p class="text-gray-600 dark:text-gray-400 max-w-xs transition-colors duration-500">
            Building digital experiences with passion and precision.
          </p>
        </div>

        <div class="md:col-span-4 lg:col-span-2">
          <h3 class="font-semibold text-gray-900 dark:text-white mb-4 transition-colors duration-500">Navigation</h3>
          <ul class="space-y-3">
            <li>
              <NuxtLink to="#about"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                About</NuxtLink>
            </li>
            <li>
              <NuxtLink to="#projects"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                Projects</NuxtLink>
            </li>
            <li>
              <NuxtLink to="#experience"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                Experience</NuxtLink>
            </li>
            <li>
              <NuxtLink to="mailto:dewacahaya30@gmail.com"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                Contact</NuxtLink>
            </li>
          </ul>
        </div>

        <div class="md:col-span-4 lg:col-span-2">
          <h3 class="font-semibold text-gray-900 dark:text-white mb-4 transition-colors duration-500">Connect</h3>
          <ul class="space-y-3">
            <li>
              <NuxtLink to="mailto:dewacahaya30@gmail.com"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                Email</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                Resume</NuxtLink>
            </li>
            <li>
              <NuxtLink to="#"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                Blog</NuxtLink>
            </li>
            <li>
              <NuxtLink to="https://linkedin.com" target="_blank"
                class="text-gray-600 dark:text-gray-400 hover:text-brand-500 dark:hover:text-brand-400 transition-colors">
                LinkedIn</NuxtLink>
            </li>
          </ul>
        </div>

        <div class="md:col-span-4 lg:col-span-3 flex md:justify-end">
          <div class="flex flex-wrap gap-2">
            <UButton icon="i-simple-icons-github" color="neutral" variant="soft"
              class="rounded-xl w-10 h-10 flex items-center justify-center hover:bg-gray-200 dark:hover:bg-gray-800 transition-colors" />
            <UButton icon="i-simple-icons-linkedin" color="neutral" variant="soft"
              class="rounded-xl w-10 h-10 flex items-center justify-center hover:bg-blue-50 dark:hover:bg-blue-900/30 hover:text-blue-500 transition-colors" />
            <UButton icon="i-simple-icons-x" color="neutral" variant="soft"
              class="rounded-xl w-10 h-10 flex items-center justify-center hover:bg-gray-200 dark:hover:bg-gray-800 transition-colors" />
            <UButton icon="i-simple-icons-instagram" color="neutral" variant="soft"
              class="rounded-xl w-10 h-10 flex items-center justify-center hover:bg-pink-50 dark:hover:bg-pink-900/30 hover:text-pink-500 transition-colors" />
            <UButton icon="i-heroicons-envelope" color="neutral" variant="soft"
              class="rounded-xl w-10 h-10 flex items-center justify-center hover:bg-brand-50 dark:hover:bg-brand-900/30 hover:text-brand-500 transition-colors" />
          </div>
        </div>

      </div>

      <div
        class="pt-8 border-t border-gray-200 dark:border-gray-800 flex flex-col md:flex-row items-center justify-between gap-4 text-sm text-gray-500 dark:text-gray-400 transition-colors duration-500">
        <p>© 2026 Dewa Cahaya. All rights reserved.</p>

        <p class="flex items-center gap-1">
          <UIcon name="ic-twotone-ac-unit" class="w-4 h-4 text-sky-500" /> inspired by Bento Style in Indonesia
        </p>
      </div>

    </div>
  </footer>
</template>
