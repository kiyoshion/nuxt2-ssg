<template>
  <div class="bg-black text-yellow-50 font-serif mx-auto container">
    <img src="~/assets/img/world-copy.svg">
    <div class="px-12">
      <h1 class="text-xl">
        映画で感じる世界史
      </h1>
      <div class="flex">
        <div>
          <p class="text-7xl">
            1943
          </p>
        </div>
        <div>
          <img :src="`https://image.tmdb.org/t/p/w185${res.data.poster_path}`">
          <p>{{ res.data.title }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $axios }) {
    const res = await $axios.get('https://api.themoviedb.org/3/movie/424?api_key=b6b43bce2f19a47be787231a60995864')
    // eslint-disable-next-line no-console
    console.log(res.data)
    return {
      res
    }
  }
}
</script>
