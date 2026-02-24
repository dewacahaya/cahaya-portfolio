<template>
  <div class="flex min-h-screen bg-gray-100 dark:bg-gray-900">
    <aside class="w-64 bg-surface-darker text-white p-5 hidden md:block">
      <h2 class="text-xl font-bold font-sans mb-10 text-brand-400">
        Admin Panel
      </h2>
      <nav class="space-y-4">
        <p>Dashboard</p>
        <p>Manage Projects</p>
        <p>Logout</p>
      </nav>
    </aside>

    <main class="flex-1 p-8">
      <slot />
    </main>
  </div>
</template>
