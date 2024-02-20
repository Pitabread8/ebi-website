<template>
  <main>
    <ContentDoc v-slot="{ doc }">
      <article>
        <h1 class="mb-2 mt-8 text-center text-3xl">{{ doc.title }}</h1>
        <p class="text-center text-sm">
          {{
            `${doc.date.substring(5, 7)}/${doc.date.substring(8, 10)}/${doc.date.substring(0, 4)}`
          }}
        </p>
        <ContentRenderer
          :value="doc"
          class="absolute left-1/2 py-6 w-1/2 translate-x-[-50%] text-justify"
        />
      </article>
    </ContentDoc>
  </main>
</template>
