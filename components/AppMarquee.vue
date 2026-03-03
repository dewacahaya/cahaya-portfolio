<template>
  <div class="pt-6 pb-3 w-full overflow-hidden">

    <UMarquee class="p-8 marquee-mask" :pause-on-hover="true">

      <UIcon name="i-logos-html-5"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />
      <UIcon name="i-logos-css-3"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />

      <UIcon name="i-logos-javascript"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />

      <UIcon name="i-logos-vue"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />
      <UIcon name="i-logos-nuxt-icon"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />
      <UIcon name="i-logos-tailwindcss-icon"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />

      <UIcon name="i-logos-bootstrap"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />


      <UIcon name="i-logos-firebase"
        class="size-18 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />
      <UIcon name="i-logos-git-icon"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />
      <UIcon name="i-logos-figma"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />

      <UIcon name="i-logos-laravel"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />
      <UIcon name="i-logos-php"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />
      <UIcon name="i-logos-mysql"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />

      <UIcon name="i-logos-pinia"
        class="size-12 mx-6 shrink-0 grayscale opacity-70 hover:grayscale-0 hover:opacity-100 transition-all duration-300 cursor-pointer" />

    </UMarquee>
  </div>
</template>

<style scoped>
/* Trik CSS Masking:
  Mengubah transparansi elemen berdasarkan gradient.
  Bagian hitam (black) = terlihat jelas.
  Bagian transparan (transparent) = tembus pandang (membaur dengan BG apapun).
*/
.marquee-mask {
  -webkit-mask-image: linear-gradient(to right, transparent, black 15%, black 85%, transparent);
  mask-image: linear-gradient(to right, transparent, black 15%, black 85%, transparent);
}
</style>
