<template>
  <div class="m-8 dark:text-white">
    <TheHeader />
    <Editor />
    <div class="dark:text-white">
      <div class="font-bold text-xl m-4">{{ $t('about_blog') }}</div>
      <div class="font-bold text-lg m-4">{{ $t('what_how_why') }}</div>
      <div class="max-w-xxl m-2 rounded overflow-hidden shadow-lg">
        <img class="w-full" src="/ois.jpg" alt="Ojciec i syn" />
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">{{ $t('blog') }}</div>
          <p class="text-base">
            {{ $t('blog_start') }}
          </p>
          <p class="text-base">
            {{ $t('blog_creating') }}
          </p>
          <p class="text-base">
            {{ $t('about_versions') }}
          </p>
          <p class="text-base">
            {{ $t('v_1.1') }}
          </p>
          <p class="text-base">
            {{ $t('v_1.2') }}
          </p>
          <p class="text-base">
            {{ $t('v_1.3') }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
