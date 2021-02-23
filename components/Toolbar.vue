<template>
  <header class="toolbar bg-gray-100 border border-gray-300 shadow-lg">
    <div class="max-w-screen-xl mx-auto px-8 py-4 flex justify-between">
      <div class="w-1/2 flex justify-start align-center">
        <Logo class="mr-8" />
        <h1
          class="title text-xl hidden lg:block font-display mt-1 font-bold text-teal-500"
        >
          Mi portafolio molón
        </h1>
      </div>
      <nav class="w-1/2">
        <ul class="flex justify-end">
          <li v-for="nav of navigation" :key="nav.label">
            <NuxtLink
              :to="nav.route"
              class="inline-block px-3 py-2 rounded-md text-md font-medium hover:bg-gray-300"
              >{{ nav.label }}</NuxtLink
            >
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
const data = () => ({
  navigation: [
    {
      label: 'Home',
      route: '/',
    },
    {
      label: 'Blog',
      route: '/blog',
    },
    {
      label: 'Portafolio',
      route: '/portfolio',
    },
    {
      label: 'Acerca',
      route: '/about',
    },
    {
      label: 'Contactame',
      route: '/contact',
    },
  ],
});
export default {
  name: 'toolbar',
  data,
};
</script>

<style>
/* home route and active route will show in bold as it matches / and /about */
a.nuxt-link-active {
  @apply font-bold;
}
/* exact link will show the primary color for only the exact matching link */
a.nuxt-link-exact-active {
  @apply text-teal-600;
}
</style>
