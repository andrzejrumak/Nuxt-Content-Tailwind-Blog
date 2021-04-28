<template>
  <div>
    <div>
      <h1 class="text-4xl">{{ $t('message') }}</h1>
    </div>
    <div class="contener mb-8 md:grid grid-cols-2 justify-items-center">
      <img src="/icon.png" class="m-3" />
      <div>
        <div class="text-4xl text-center">
          <p>{{ $t('blog') }}</p>
          <div class="text-2xl m-3">
            {{ $t('blog_welcome') }}
          </div>
        </div>
        <!--div class="text-4xl text-center">
          Web Development
          <div class="text-2xl m-3">
            Stronę tę tworzę samodzielnie w oparciu o najnowsze rozwiązania w
            programowaniu stron i aplikacji internetowych.
          </div>
        </div -->
      </div>
    </div>
  </div>
</template>
