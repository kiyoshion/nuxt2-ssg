<template>
  <div>
    <div>
      <h2>BOOKS</h2>
      <ul>
        <li v-for="(b, i) in books" :key="i">
          <nuxt-link :to="`/books/${b.slug}`">
            {{ b.title }}
          </nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const books = await $content('books')
      .limit(5)
      .fetch()

    return {
      books
    }
  }
}
</script>
