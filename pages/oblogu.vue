<template>
  <div class="m-8">
    <TheHeader />
    <Editor />
    <div class="font-bold text-xl m-4">O blogu</div>
    <div class="font-bold text-lg m-4">Co? Jak? Dlaczego?</div>
    <div class="max-w-xl m-2 rounded overflow-hidden shadow-lg">
      <img class="w-full" src="/ois.jpg" alt="Ojciec i syn" />
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">Blog Jestem Ojcem</div>
        <p class="text-gray-700 text-base">
          Blog ten powstał w szczególnym dniu, w którym moja dorosła córka i syn
          obronili pracę dyplomową. Jest to też rozszerzenie dla strony na
          Facebook o tym samym tytule.
        </p>
        <p class="text-gray-700 text-base">
          Stronę tą tworzę samodzielnie w frameworku Nuxt JS.
        </p>
        <p class="text-gray-700 text-base">
          Kolejne wersje strony i jej nowe funkcjonalności.
        </p>
        <p class="text-gray-700 text-base">
          Wersja 1.1: Dodanie wersji dark do czytania w nocy.
        </p>
        <p class="text-gray-700 text-base">
          Wersja 1.2: Rozszerzenie o wersje PWA (Progressiw Web Application), która daje możliwość czytania bloga offline
        </p>
      </div>
    </div>
  </div>
</template>