<template>
  <div class="bg-barcamp my-5 py-5">
    <b-container>
      <b-jumbotron class="text-center text-white bg-barcamp">
        <template v-slot:header>Oops! This page is still in development</template>
        <template v-slot:lead>
          {{ error.statusCode }} Page not found | Sorry for the inconvenience
        </template>
        <hr class="my-4">
        <b-button href="/" variant="outline-light" size="md" class="abt-btn p-3 mr-1" pill>
          Go back to home
        </b-button>
      </b-jumbotron>
    </b-container>
  </div>
</template>

<script>
export default {
  layout: 'error-layout',
  props: {
    error: Object,
    default: null
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
  background-image: url('~assets/img/bg-barcamp.jpg');
  background-size: cover;
  background-attachment: fixed;
}
</style>
