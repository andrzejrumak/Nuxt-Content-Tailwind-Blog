<template>
  <div>
    <header class="p-3 flex">
      <NuxtLink :to="localePath('index')"><Logo class="mb-4" /></NuxtLink>
      <NuxtLink :to="localePath('/oblogu')">{{ $t('about') }}</NuxtLink>
      <!--AppSearchInput class="ml-8" /-->
      <LangInput class="ml-2 mb-4 border-2 rounded-md p-1 border-black" />
      <button
        class="ml-2 mb-4 border-2 rounded-md p-1 border-black"
        @click="toggle"
      >
        {{ $colorMode.preference }}
      </button>
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
