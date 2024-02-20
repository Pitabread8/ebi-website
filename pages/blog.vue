<script setup>
const { data: articles } = await useAsyncData("blog", () =>
  queryContent("/blog").sort({ date: 1 }).find(),
);
</script>

<template>
  <main>
    <h1 class="m-8 text-center text-3xl">Articles</h1>
    <div
      class="absolute left-1/2 grid w-3/4 translate-x-[-50%] gap-6 md:grid-cols-3"
    >
      <NuxtLink
        v-for="article in articles"
        :key="article._path"
        :to="article._path"
        class="flex w-full flex-col gap-3 p-4"
      >
        <p class="px-1 text-sm">
          {{
            `${article.date.substring(5, 7)}/${article.date.substring(8, 10)}/${article.date.substring(0, 4)}`
          }}
        </p>
        <NuxtImg :src="'/blog/' + article.image" class="rounded-2xl" />
        <h2 class="px-1 text-xl">{{ article.title }}</h2>
      </NuxtLink>
    </div>
  </main>
</template>
