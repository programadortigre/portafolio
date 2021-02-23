<template>
  <article>
    <h2 class="font-display font-bold text-4xl mb-16 text-gray-800">
      {{ project.title }}
    </h2>
    <figure class="mb-4">
      <img :src="project.media" alt="" />
    </figure>

    <NuxtContent
      class="prose prose-sm sm:prose lg:prose-lg xl:prose-2xl "
      :document="project"
    />
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const slug = params.slug;
    const project = await $content('portfolio', slug).fetch();

    return {
      project,
    };
  },
};
</script>

<style></style>
