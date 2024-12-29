<template>
  <article>
    <ContentDoc />
  </article>
</template>

<script lang="ts" setup>
const route = useRoute();
console.log(route.params.slug);
</script>
