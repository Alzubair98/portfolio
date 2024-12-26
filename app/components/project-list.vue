<template>
  <div>
    <p class="mb-10">Take a look at my GitHub projects!</p>

    <section v-if="pending">Loading...</section>
    <section v-else-if="error">Error... Try again</section>
    <section v-else>
      <ul class="grid grid-cols-1 gap-4">
        <li
          v-for="repo in data"
          :key="repo.id"
          class="border border-gray-200 rounded-sm p-4 hover:bg-gray-200 font-mono"
        >
          <a :href="repo.html_url" target="_blank">
            <div class="flex items-center justify-between text-sm">
              <div class="font-semibold">{{ repo.name }}</div>
              <div>{{ repo.stargazers_count }} ★</div>
            </div>
            <p class="text-sm">{{ repo.description }}</p>
          </a>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup lang="ts">
interface GitHubRepo {
  [key: string]: any; // Include additional properties if needed
}

const githubURL = "https://api.github.com/users/Alzubair98/repos";

const { error, pending, data } = await useFetch<GitHubRepo[]>(githubURL);
</script>
