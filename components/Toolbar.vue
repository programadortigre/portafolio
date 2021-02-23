<template>
  <header class="toolbar bg-gray-200 border border-gray-300">
    <div class="max-w-7xl mx-auto px-8 py-4 flex justify-between">
      <Logo />
      <nav></nav>
    </div>
  </header>
</template>

<script>
const data = () => ({
  navigation: [
    {
      label: "Home",
      slug: "home"
    }
  ]
});
export default {
  name: "toolbar",
  data
};
</script>

<style></style>
