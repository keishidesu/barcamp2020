<template>
  <b-row class="mt-5 pt-4 text-center">
    <b-col
      v-for="(card,i) in cards"
      :key="`card-${i}`"
      cols="6"
      lg="4"
      class="mt-4"
    >
      <b-img
        :src="`${base}icon/${card.image}.png`"
        style="width:auto; height:12em"
        fluid
      />
      <b-card-text class="mt-2 roboto-light text-purple mt-3" style="line-height:1.5em;">
        {{ card.caption }}
      </b-card-text>
    </b-col>
  </b-row>
</template>

<script>
export default {
  data: () => {
    return {
      base: process.env.base,
      cards: [
        {
          image: 'audspe',
          caption: 'Choose to be an audience or speaker'
        },
        {
          image: 'choose',
          caption: 'Choose who get to speak'
        },
        {
          image: 'tal',
          caption: 'Choose which talks to attend'
        },
        {
          image: 'awa',
          caption: 'Get awards for your talk'
        },
        {
          image: 'boa',
          caption: 'Activites or games in the lobby room'
        },
        {
          image: 'luc',
          caption: 'Lucky Draw'
        }
      ]
    }
  }
}
</script>

<style>

</style>
