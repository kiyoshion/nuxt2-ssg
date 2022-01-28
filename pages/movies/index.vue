<template>
  <div class="bg-black text-yellow-50 py-8 relative">
  <!-- <div class=" py-8 relative"> -->
    <h1 class="text-4xl mb-8 mx-auto container font-serif">
      映画で感じる世界史
    </h1>
    <ul class="mx-auto mb-4 container flex ">
      <li>World War Ⅱ</li>
    </ul>
    <div class="flex font-serif mx-auto container">
      <div class="mr-8 w-2/4 static z-20">
        <div class="flex">
          <div>
            <p class="text-4xl mr-4">
              1939
            </p>
            <p>
              <span class="text-2xl my-4 mr-4 inline-block">9.1</span>
              ナチス・ドイツによるポーランド侵攻
            </p>
            <div v-for="(m, i) in res.data" :key="i">
              <movie-desc :movie="m" class="flex " />
            </div>
          </div>
          <!-- <div class="flex flex-col">
            <div v-for="(m, i) in res.data" :key="i">
              <movie-desc :movie="m" />
            </div>
          </div> -->
        </div>
      </div>
      <world-map class="w-3/4 fixed top-0 right-0 z-10 mt-4" />
      <!-- <img class="w-2/4" src="~/assets/img/world-copy.svg"> -->
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $axios }) {
    // const res = await $axios.get('https://api.themoviedb.org/3/movie/424?api_key=b6b43bce2f19a47be787231a60995864')
    const res = await $axios.get('http://localhost/api/v1/movies')
    // eslint-disable-next-line no-console
    console.log(res.data)
    return {
      res
    }
  }
}
</script>
