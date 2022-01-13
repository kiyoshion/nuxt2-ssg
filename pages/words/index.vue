<template>
  <div>
    <h2 class="text-xl font-bold">
      著名人の単語帳
    </h2>
    <div v-for="(w, i) in words" :key="i">
      <div class="flex items-center">
        <p class="font-bold mr-4">
          {{ w.key }}({{ w.keyEn }})
        </p>
        <p class="text-sm">
          {{ w.mean }}
          <span>
            『{{ w.source.title }}』({{ w.source.authorJp }})
          </span>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import words from '@/assets/json/words.json'

export default {
  data () {
    return {
      words
    }
  },
  methods: {
    toggleMean (i) {

    }
  }
}
</script>
