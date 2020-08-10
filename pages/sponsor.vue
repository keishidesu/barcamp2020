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
    <div class="py-5 bg-pale">
      <Sponsor :simple="false" />
    </div>
  </body>
</template>

<script>
import Socialicon from '~/components/social-icons'
import Navbar from '~/components/navbar'
import Homenav from '~/components/home-nav'
import Sponsor from '~/components/sponsor'

export default {
  components: {
    Socialicon,
    Navbar,
    Homenav,
    Sponsor
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
