<template>
  <b-navbar toggleable="lg" type="dark" class="roboto">
    <b-navbar-brand href="#home">
      <b-img src="~/assets/img/barcamp-logo.png" style="height:2em" />
    </b-navbar-brand>

    <b-navbar-toggle target="home-nav-collapse" />

    <b-collapse id="home-nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto text-white">
        <b-nav-item
          v-for="(item,i) in homeitems"
          :key="`item-${i}`"
          :href="`${item.destination}`"
          class="nav-item"
        >
          {{ item.navitem }}
        </b-nav-item>
        <b-nav-item
          v-for="(item,i) in externalitems"
          :key="`item-${i}`"
          :href="`${item.destination}`"
          target="_blank"
          class="nav-item"
        >
          {{ item.navitem }}
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  props: {
    hideLogo: {
      type: Boolean,
      required: false,
      default: false
    }
  },
  data: () => {
    return {
      homeitems: [
        {
          navitem: 'Home',
          destination: '/'
        },
        {
          navitem: 'About',
          destination: '/#about'
        },
        {
          navitem: 'Agenda',
          destination: '/#agenda'
        },
        {
          navitem: 'FAQ',
          destination: '/#faq'
        },
        {
          navitem: 'Sponsors',
          destination: '/sponsor'
        },
        {
          navitem: 'Vote Results',
          destination: '/#vote'
        }
      ],
      externalitems: [
        {
          navitem: 'Register',
          destination: 'https://forms.gle/yLiydr62cgkHF2Sp9'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .nav-item {
    padding-left: 0.5em;
    padding-right: 0.5em;
    font-size: 1.2em;
  }
</style>
