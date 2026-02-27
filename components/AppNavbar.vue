<script setup lang="ts">
const colorMode = useColorMode();

// 1. Logika Toggle Dark/Light Mode
const isDark = computed({
  get() {
    return colorMode.value === "dark";
  },
  set() {
    colorMode.preference = colorMode.value === "dark" ? "light" : "dark";
  },
});

// 2. Data Navigasi (Anchor Link + Dropdown)
const links = [
  {
    label: "ABOUT",
    to: "#about", // Link ke ID Section
    icon: "i-heroicons-user",
    children: [
      { label: "My Story", to: "#about-story", icon: "i-heroicons-book-open" },
      { label: "Tech Stack", to: "#about-stack", icon: "i-heroicons-cpu-chip" },
    ],
  },
  {
    label: "PROJECTS",
    to: "#projects",
    icon: "i-heroicons-rectangle-stack",
    children: [
      { label: "Web Apps", to: "#projects-web", icon: "i-heroicons-globe-alt" },
      {
        label: "Mobile Apps",
        to: "#projects-mobile",
        icon: "i-heroicons-device-phone-mobile",
      },
      {
        label: "UI/UX Design",
        to: "#projects-design",
        icon: "i-heroicons-paint-brush",
      },
    ],
  },
  {
    label: "EXPERIENCES",
    to: "#experience",
    icon: "i-heroicons-briefcase",
    children: [
      {
        label: "Work History",
        to: "#exp-work",
        icon: "i-heroicons-building-office",
      },
      { label: "Education", to: "#exp-edu", icon: "i-heroicons-academic-cap" },
    ],
  },
];
</script>

<template>
  <header
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 bg-white/10 dark:bg-surface-darker/10 backdrop-blur-sm border-b border-gray-200 dark:border-gray-800"
  >
    <UContainer class="h-16 flex items-center justify-between">
      <div class="shrink-0">
        <NuxtLink
          to="/"
          class="text-2xl font-bold font-sans text-brand-500 tracking-tighter"
        >
          MY <span class="text-gray-800 dark:text-white">PORTFOLIO</span>.
        </NuxtLink>
      </div>

      <nav class="hidden sm:flex items-center gap-2">
        <template v-for="(item, index) in links" :key="index">
          <UDropdown
            :items="[item.children]"
            :popper="{ placement: 'bottom-start' }"
            mode="hover"
          >
            <UButton
              :to="item.to"
              variant="ghost"
              color="neutral"
              class="font-medium text-gray-600 dark:text-gray-300 hover:text-brand-500 dark:hover:text-brand-400 hover:bg-transparent"
            >
              <span class="mr-1">{{ item.label }}</span>
              <UIcon :name="item.icon" class="w-4 h-4" />
            </UButton>

            <template #item="{ item: subItem }">
              <span class="truncate">{{ subItem.label }}</span>
              <UIcon
                :name="subItem.icon"
                class="shrink-0 w-4 h-4 text-gray-400 ms-auto"
              />
            </template>
          </UDropdown>
        </template>
      </nav>

      <div class="flex items-center gap-2">
        <ClientOnly>
          <button
            class="relative flex items-center h-8 w-14 rounded-full transition-colors duration-300 focus:outline-none focus:ring-2 focus:ring-brand-500 focus:ring-offset-2 dark:focus:ring-offset-gray-900"
            :class="
              isDark ? 'bg-surface-dark border border-gray-700' : 'bg-gray-200'
            "
            @click="isDark = !isDark"
          >
            <span class="sr-only">Toggle Dark Mode</span>
            <span
              class="w-6 h-6 transform bg-white rounded-full shadow-md transition-transform duration-300 flex items-center justify-center"
              :class="isDark ? 'translate-x-7' : 'translate-x-1'"
            >
              <UIcon
                v-if="!isDark"
                name="i-heroicons-sun"
                class="w-4 h-4 text-orange-500"
              />
              <UIcon
                v-else
                name="i-heroicons-moon"
                class="w-4 h-4 text-brand-500"
              />
            </span>
          </button>
        </ClientOnly>

        <USlideover>
          <UButton
            icon="i-heroicons-bars-3"
            color="neutral"
            variant="ghost"
            class="sm:hidden ml-2"
          />

          <template #content="{ close }">
            <div
              class="flex flex-col h-full bg-surface-light dark:bg-surface-darker"
            >
              <div
                class="flex items-center justify-end p-4 border-b border-gray-200 dark:border-gray-800"
              >
                <UButton color="neutral" variant="ghost" @click="close">
                  <UIcon
                    name="i-heroicons-x-mark-20-solid"
                    class="w-8 h-8 text-gray-500 hover:text-brand-500 transition-colors"
                  />
                </UButton>
              </div>

              <div class="flex flex-col gap-2 p-4">
                <UButton
                  v-for="item in links"
                  :key="item.label"
                  :to="item.to"
                  variant="ghost"
                  color="neutral"
                  class="justify-start text-lg font-medium text-gray-600 dark:text-gray-300 hover:text-brand-500 dark:hover:text-brand-400"
                  @click="close"
                >
                  <UIcon :name="item.icon" class="w-5 h-5 mr-3" />
                  <span>{{ item.label }}</span>
                </UButton>
              </div>
            </div>
          </template>
        </USlideover>
      </div>
    </UContainer>
  </header>
</template>

<style scoped>
.router-link-active {
  color: var(--color-brand-400);
}
</style>
