<template>
  <div class="container">
    <div>
      <Logo class="mx-auto" />
      <h1 class="title m-4 text-xl font-display font-bold text-teal-500">
        Mi portafolio molón
      </h1>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
