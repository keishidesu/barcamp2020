<template>
  <b-card
    no-body
    :style="{
      border: (simple) ? 'none' : `1rem outset #${getColor(tier)}`
    }"
    class="text-center mt-4"
  >
    <div v-if="!simple" class="position-absolute" style="top: 5px; right: 10px">
      <b-badge :style="{ backgroundColor: `#${getColor(tier)}` }" style="color: rgba(0, 0, 0, 0.5);">
        {{ tier }}
      </b-badge>
    </div>
    <b-card-body>
      <a :href="`${websiteUrl}`" target="_blank">
        <b-img
          rounded
          fluid
          :src="`/sponsor/${imageUrl}.jpg`"
          :width="250"
        />
      </a>
    </b-card-body>
    <b-card-footer v-if="!simple" class="border-0 rounded" :style="{ backgroundColor: `#${getColor(tier)}14` }">
      <b>{{ name }}</b>
    </b-card-footer>
  </b-card>
</template>

<script>
export default {
  props: {
    simple: {
      type: Boolean,
      required: false,
      default: true
    },
    imageUrl: {
      type: String,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    tier: {
      type: String,
      required: true
    },
    websiteUrl: {
      type: String,
      required: true
    }
  },
  methods: {
    getColor (tier) {
      if (tier === 'Platinum') {
        return 'e6feff'
      } else if (tier === 'Gold') {
        return 'fff0b5'
      } else if (tier === 'Silver') {
        return 'E6E6FA'
      } else {
        return 'e0d0bc'
      }
    }
  }
}
</script>
