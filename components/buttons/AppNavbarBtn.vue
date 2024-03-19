<template>
  <div>
    <NuxtLink to="/aboutUs" class="px-6 py-4 m-2 md:m-0 rounded-full uppercase text-white font-medium border transition-all duration-300 hover:bg-gray-400 hover:text-black hover:border-gray-400">
      <slot></slot>
    </NuxtLink>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.route-link-active {
  @apply bg-gray-400 border-gray-400;
}
</style>
