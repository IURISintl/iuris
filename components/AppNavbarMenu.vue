<template>
  <div class="flex flex-col md:flex-row space-y-2 md:space-x-4 text-white uppercase md:px-2 md:py-5 md:border md:rounded-full font-medium">
    <NuxtLink to="/" class="active link-animation px-6 py-4">the firm</NuxtLink>
    <NuxtLink to="/legalAi" class="link-animation px-6 py-4">legal ai</NuxtLink>
    <NuxtLink to="/insights" class="link-animation px-6 py-4">insights</NuxtLink>
    <NuxtLink to="/consult" class="link-animation px-6 py-4">consult</NuxtLink>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.link-animation {
  transition: 0.5s;
}
.link-animation:hover {
  @apply bg-gray-400 rounded-full;
}

.route-link-active {
  @apply bg-gray-400  rounded-full relative pl-10;
}
.route-link-active::before {
  content: "";
  position: absolute;
  height: 10px;
  width: 10px;
  top: 50%;
  transform: translateY(-50%);
  left: 20px;
  border-radius: 999px;
  background-color: white;
}
</style>
