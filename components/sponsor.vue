<template>
  <b-container>
    <h3>
      <b class="roboto-fat text-purple text-title">Sponsors</b>
    </h3>
    <b-row class="mt-3">
      <b-col v-for="(sponsor, key) in sponsors" :key="`sponsor-${key}`" align-self="center">
        <b-img :src="`/sponsor/${sponsor.img}.jpg`" fluid />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import { sponsors } from '~/assets/json/sponsor.json'

export default {
  data: () => {
    return {
      sponsors
    }
  }
}
</script>
