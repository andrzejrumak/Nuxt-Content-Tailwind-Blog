<template>
  <div>
    <header class="p-3 flex">
      <NuxtLink to="/"><Logo class="mb-4" /></NuxtLink>
      <NuxtLink to="/oblogu">O blogu</NuxtLink>
      <AppSearchInput class="ml-8" />
      <button
        class="ml-2 mb-4 border-2 rounded-md p-1 border-black"
        @click="toggle"
      >
        {{ $colorMode.preference }}
      </button>
      <LangInput class="ml-2 mb-4 border-2 rounded-md p-1 border-black" />
    </header>
    <MainContent />
  </div>
</template>
<script>
import LangInput from './LangInput.vue'
export default {
  components: { LangInput },
  methods: {
    toggle() {
      this.$colorMode.preference =
        this.$colorMode.value == 'light' ? 'dark' : 'light'
    }
  }
}
</script>
