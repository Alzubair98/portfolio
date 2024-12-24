<template>
  <div>
    <h2>Projects</h2>
  </div>
</template>

<script setup lang="ts">
const githubURL = "https://api.github.com/users/Alzubair98/repos";
const { data } = await useFetch(githubURL);

console.log(data.value);
</script>
