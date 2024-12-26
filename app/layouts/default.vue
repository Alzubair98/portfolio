<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex justify-between items-center">
      <div class="flex items-center space-x-12">
        <div>
          <NuxtLink to="/" class="text-xl font-semibold p-2 hover:bg-gray-200"
            >Alzubair</NuxtLink
          >
        </div>

        <Menu />
      </div>
      <ClientOnly>
        <color-mode-selector />
      </ClientOnly>
    </header>

    <main class="p-2">
      <slot />
    </main>
  </div>
</template>

<script setup>
useHead({
  titleTemplate: "%s - Alzubair Alqaraghuli",
  link: [
    {
      rel: "preconnect",
      href: "https://fonts.googleapis.com",
    },
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css2?family=Roboto&display=swap",
      crossorigin: "",
    },
  ],
});
</script>

<style>
body {
  font-family: "Roboto";
}

body {
  @apply bg-white dark:bg-gray-900 text-gray-700 dark:text-gray-300;
}
</style>
