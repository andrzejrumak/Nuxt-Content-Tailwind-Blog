<template>
  <header class="pt-3 flex">
    <NuxtLink to="/"><Logo class="mb-4 " /></NuxtLink>
    <NuxtLink to="/oblogu">O blogu</NuxtLink>
    <AppSearchInput class="ml-8" />
    <button @click="toggle" class=" ml-2 mb-4 border-2 rounded-md p-1 border-black" >{{ $colorMode.preference }}</button>
  </header>
</template>
<script>
export default {
  methods:{
    toggle() {
    this.$colorMode.preference =
      this.$colorMode.value == "light" ? "dark" : "light";
    }
  }
}
</script>