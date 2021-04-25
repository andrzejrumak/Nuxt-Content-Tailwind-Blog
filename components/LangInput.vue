<template>
  <div class="text-white bg-black p-3">
    <select v-model="$i18n.locale" class="text-white bg-black">
      <option
        v-for="lang in $i18n.locales"
        :key="lang.code"
        :value="lang.code"
        class="text-white bg-black"  
        >{{ lang.name }}</option
      >
    </select>
  </div>
</template>

<script>
export default {}
</script>