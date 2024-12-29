<template>
  <div>
    <div>We are inside a blog</div>
    <div>Post id is {{ route.params.slug }}</div>
  </div>
</template>

<script lang="ts" setup>
const route = useRoute();
console.log(route.params.slug);
</script>
