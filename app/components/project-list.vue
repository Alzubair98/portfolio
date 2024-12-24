<template>
  <div>
    <h2>Projects</h2>
  </div>

  <section v-if="pending">Loading...</section>
  <section v-else-if="error">Error... Try again</section>
  <section v-else>Repos!!</section>
</template>

<script setup lang="ts">
const githubURL = "https://api.github.com/users/Alzubair98/repos";

const { error, pending, data } = await useFetch(githubURL);
</script>
