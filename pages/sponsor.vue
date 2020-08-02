<template>
  <body>
    <div id="social-icon" class="d-none d-md-block">
      <socialicon />
    </div>
    <div class="bg-barcamp">
      <b-container>
        <Homenav />
      </b-container>
      <div id="nav">
        <navbar />
      </div>
    </div>
    <div id="sponsor-card">
      <SponsorCard />
    </div>
  </body>
</template>

<script>
import Socialicon from '~/components/social-icons'
import Navbar from '~/components/navbar'
import Homenav from '~/components/home-nav'
import SponsorCard from '~/components/sponsor/sponsor-card'

export default {
  components: {
    Socialicon,
    Navbar,
    Homenav,
    SponsorCard
  }
}

window.onscroll = function () {
  scrollFunction()
}

function scrollFunction () {
  if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
    document.getElementById('nav').style.top = '0'
  } else {
    document.getElementById('nav').style.top = '-70px'
  }
}
</script>

<style scoped>
  #nav {
  width: 100%;
  position: fixed;
  top: -70px;
  display: block;
  transition: top 0.3s;
  z-index: 9999;
}
</style>
