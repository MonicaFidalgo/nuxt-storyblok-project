<template>
  <div v-editable="blok" class="py-8 mb-6">
    <div class="relative">
      <h2 class="relative font-serif text-4xl z-10">{{ blok.title }}</h2>
      <div class="absolute top-0 w-64 h-10 mt-6 bg-yellow-300 opacity-50"></div>
    </div>
    <ul class="flex -mx-8">
      <li v-for="article in blok.articles" :key="article._uid">
        <article-teaser
          v-if="article.content"
          :article-content="article.content"
        ></article-teaser>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true,
    },
  },
};
</script>
