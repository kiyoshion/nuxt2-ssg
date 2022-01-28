<template>
  <div class="flex mb-4 items-start">
    <img class="w-20 mr-2 object-contain" :src="`http://localhost/storage/img/movie${movie.poster_path}`">
    <!-- <div>
      <p class="text-xl">{{ movie.title }}</p>
      <p class="text-sm">{{ movie.overview_ja }}</p>
    </div> -->
  </div>
</template>

<script>
export default {
  props: {
    // eslint-disable-next-line vue/require-default-prop
    movie: {
      type: Object
    }
  }
}
</script>
