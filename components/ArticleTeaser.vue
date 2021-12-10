<template>
  <a href="#" class="blok py-10">
    <img :src="articleContent.hero_image.filename" class="pb-10" />
    <h2 class="pb-6 text-xl">{{ articleContent.intro }}</h2>
    <p class="pb-6 text-gray-700 leading-loose">
      {{ articleContent.intro }}
    </p>
    <p class="text-gray-700">
      {{ articleContent.author }}
    </p>
  </a>
</template>

<script>
export default {
  props: {
    articleContent: {
      type: Object,
      required: true,
    },
  },
};
</script>
