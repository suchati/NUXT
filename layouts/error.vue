<template>
  <v-layout align-center justify-center fill-height>
    <div class="text-center">
      <h1 class="font-weight-black text-h2">
        {{ error.statusCode === 404 ? pageNotFound : otherError }}
      </h1>
      <br>
      <v-btn to="/">
        Go To Home page
      </v-btn>
    </div>
  </v-layout>
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  data: () => ({
    pageNotFound: '404 Not Found',
    otherError: 'An error occurred'
  })
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
