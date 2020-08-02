<template>
  <b-container class="py-5">
    <div class="py-1" style="font-size:3rem">Sponsors</div>
    <div v-for="(sponsor, key) in sponsors" :key="`sponsor-${key}`" class="py-3">
      <b-card class="bg-pale border-0 shadow">
        <b-row>
          <b-col md="3" class="text-center mb-3" align-self="center">
            <b-img :src="`/sponsor/${sponsor.img}.png`" img-left width="250" fluid />
          </b-col>
          <b-col align-self="center">
            <b-card-title>
              {{ sponsor.company }}
              <b-badge :style="`background-color:#${sponsor.color}`" pill>{{ sponsor.tier }}</b-badge>
            </b-card-title>
            <b-card-text v-for="(desc, key) in sponsor.desc" :key="`desc-${key}`">
              {{ desc }}
            </b-card-text>
            <a :href="`${sponsor.href}`" target="_blank">
              <b-button variant="outline-dark">Visit Website</b-button>
            </a>
          </b-col>
        </b-row>
      </b-card>
    </div>
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

<style>

</style>
