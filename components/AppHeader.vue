<template>
  <div class="p-4 md:p-6 bg-black md:flex md:justify-between md:items-center relative z-10">
    <div class="flex justify-between items-center md:block">
      <NuxtLink href="/"><img src="~/assets/image/iuris-white.png" alt="iuris logo" class="h-14" /></NuxtLink>
      <div class="text-white block md:hidden cursor-pointer" @click="toggleNavbar">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="white" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </div>
    </div>
    <AppNavbarMenu class="hidden md:block"></AppNavbarMenu>
    <ButtonsAppNavbarBtn class="hidden md:block">About Us</ButtonsAppNavbarBtn>
  </div>
  <div class="bg-black md:hidden transition-all duration-500" :class="{ open: isOpen, close: !isOpen }">
    <AppNavbarMenu></AppNavbarMenu>
    <ButtonsAppNavbarBtn class="pt-4 pb-6 mt-2">About Us</ButtonsAppNavbarBtn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleNavbar() {
      this.isOpen = !this.isOpen;
    },
  },
  watch: {
    $route() {
      this.isOpen = false;
    },
  },
};
</script>

<style scoped>
.open {
  display: block;
}
.close {
  margin-top: -320px;
}
</style>
