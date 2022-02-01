<template>
  <div class="container mx-auto flex justify-between">
    <nuxt-link to="/">
      LOGO
    </nuxt-link>
    <ul class="flex">
      <li>
        <nuxt-link to="/books">
          BOOKS
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/movies">
          MOVIES
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/pg">
          PROGRAMMING
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/words">
          WORDS
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<style scoped>
a {
  padding: 0 .5rem;
}
</style>
