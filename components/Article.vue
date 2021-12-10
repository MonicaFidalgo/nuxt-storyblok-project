<template>
  <div v-editable="blok" class="prose my-24 mx-auto">
    <h1>{{ blok.author }}</h1>
    <p>{{ blok.intro }}</p>
    <img :src="blok.hero_image.filename" />
    {{ blok }}
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
