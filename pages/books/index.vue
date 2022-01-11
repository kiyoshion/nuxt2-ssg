<template>
  <div>
    <h1>名著を読みあさる</h1>
    <ul>
      <li v-for="(a, i) in articles" :key="i">
        <nuxt-link :to="`/books/${a.slug}`">
          {{ a.title }}
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const articles = await $content('books')
      .fetch()

    return {
      articles
    }
  }
}
</script>
