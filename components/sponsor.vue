<template>
  <b-container>
    <h3 class="pb-3">
      <b class="roboto-fat text-purple text-title">Sponsors &#38; Partners</b>
    </h3>
    <b-row class="mt-3">
      <b-col
        v-for="(sponsor, key) in sponsors"
        :key="`sponsor-${key}`"
        cols="12"
        md="4"
        class="h-100"
        align-self="center"
      >
        <SponsorCard
          :simple="simple"
          :name="sponsor.company"
          :tier="sponsor.tier"
          :image-url="sponsor.img"
          :website-url="sponsor.href"
        />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import { sponsors } from '~/assets/json/sponsor.json'
import SponsorCard from '~/components/sponsor/sponsor-card'

export default {
  components: {
    SponsorCard
  },
  props: {
    simple: {
      type: Boolean,
      required: false,
      default: true
    }
  },
  data: () => {
    return {
      sponsors
    }
  }
}
</script>
