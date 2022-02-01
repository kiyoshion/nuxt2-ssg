<template>
  <div>
    <h1>プログラミング</h1>
    <ul>
      <li @click="filter(0)">
        爆訳
      </li>
    </ul>
    <ul>
      <li v-for="(a, i) in articles" :key="i">
        <nuxt-link :to="`/pg/${a.slug}`">
          {{ a.title }}
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const articles = await $content('pg')
      .fetch()

    return {
      articles
    }
  },
  methods: {
    filter (n) {

    }
  }
}
</script>
