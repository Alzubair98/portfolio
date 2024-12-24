<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex justify-between">
      <div>
        <NuxtLink to="/" class="text-xl font-semibold p-2 hover:bg-gray-200"
          >Alzubair</NuxtLink
        >
      </div>
    </header>
    <nav>
      <ul>
        <li>
          <NuxtLink to="/">Main</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About</NuxtLink>
        </li>
      </ul>
    </nav>
    <slot />
  </div>
</template>
