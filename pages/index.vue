<template>
  <div class="p-8">
    <TheHeader />
    <h1 class="font-bold text-4xl dark:text-white m-8">{{ $t('articles') }}</h1>
    <ul class="flex flex-wrap">
      <li
        v-for="article of articles"
        :key="article.slug"
        class="xs:w-full md:w-1/2 px-2 xs:mb-6 md:mb-12 article-card bg-blue-800 hover:opacity-50"
      >
        <NuxtLink
          :to="
            localePath({ name: 'blog-slug', params: { slug: article.slug } })
          "
          class="flex transition-shadow duration-150 ease-in-out shadow-sm hover:shadow-xl xxlmax:flex-col"
        >
          <img
            v-if="article.img"
            class="h-48 xxlmin:w-1/2 xxlmax:w-full object-cover"
            :src="article.img"
          />

          <div
            class="p-6 flex flex-col justify-between xxlmin:w-1/2 xxlmax:w-full dark:text-white dark:bg-black"
          >
            <h2 class="font-bold">{{ article.title }}</h2>
            <p>by {{ article.author.name }}</p>
            <p class="font-bold text-gray-600 text-sm">
              {{ article.description }}
            </p>
          </div>
        </NuxtLink>
      </li>
    </ul>
    <h3 class="mb-4 font-bold text-2xl uppercase text-center">
      {{ $t('topics') }}
    </h3>
    <ul class="flex flex-wrap mb-4 text-center">
      <li
        v-for="tag of tags"
        :key="tag.slug"
        class="xs:w-full md:w-1/3 lg:flex-1 px-2 text-center"
      >
        <NuxtLink :to="localePath(`/blog/tag/${tag.slug}`)" class="">
          <p class="font-bold text-gray-600 uppercase tracking-wider text-ss">
            {{ tag.name }}
          </p>
        </NuxtLink>
      </li>
    </ul>
    <footer class="flex justify-center border-gray-500 border-t-2">
      <p class="mt-4">
        Created by
        <a
          href="https://twitter.com/RumakAndrzej"
          class="font-bold hover:underline"
          >Andrzej Rmak</a
        >
        at NuxtJS. Special thanks for
        <a
          href="https://twitter.com/debs_obrien"
          class="font-bold hover:underline"
          >Debs Obrien</a
        >
        for
        <a
          href="https://nuxtjs.org/blog/creating-blog-with-nuxt-content"
          class="font-bold hover:underline"
          >tutorial.</a
        >
      </p>
    </footer>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, app, params, route, redirect }) {
    console.log(app.i18n.locale)
    console.log(params.slug)
    const articles = await $content(`${app.i18n.locale}/articles`, params.slug)
      .only(['title', 'description', 'img', 'slug', 'author'])
      .sortBy('createdAt', 'desc')
      .fetch()
    const tags = await $content(`${app.i18n.locale}/tags`, params.slug)
      .only(['name', 'description', 'img', 'slug'])
      .sortBy('createdAt', 'asc')
      .fetch()
    return {
      articles,
      tags
    }
  }
}
</script>

<style class="postcss">
.article-card {
  border-radius: 8px;
}
.article-card a {
  background-color: #fff;
  border-radius: 8px;
}
.article-card img div {
  border-radius: 8px 0 0 8px;
}
</style>
