<template>
  <div>
    <h1>
      {{ page.title }}
    </h1>
    <div>
      <nuxt-content :document="page" />
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const page = await $content('pg', params.slug)
      .fetch()

    return {
      page
    }
  }
}
</script>
