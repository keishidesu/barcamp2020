<template>
  <body>
    <div id="social-icon" class="d-none d-md-block">
      <socialicon />
    </div>

    <div class="bg-barcamp">
      <div id="nav">
        <navbar />
      </div>

      <div id="home">
        <home />
      </div>
    </div>

    <div id="tcd">
      <tcd />
    </div>

    <div class="bg-pale">
      <b-container>
        <div id="about" class="pt-5 pb-5">
          <about />
        </div>
      </b-container>
    </div>

    <!-- <div id="register" class="bg-barcamp">
      <register />
    </div> -->

    <div id="agenda" class="pt-5 pb-5">
      <Agenda />
    </div>

    <div id="vote" class="pt-5 pb-5">
      <Voting />
    </div>

    <div id="faq" class="pt-5 pb-5">
      <faq />
    </div>

    <div id="carousel">
      <carousel />
    </div>

    <div id="sponsor" class="pt-5 pb-5">
      <sponsor />
    </div>
  </body>
</template>

<script>
import Socialicon from '~/components/social-icons'
import Navbar from '~/components/navbar'
import Home from '~/components/home'
import About from '~/components/about'
import Carousel from '~/components/carousel'
import Voting from '~/components/voting'
import Faq from '~/components/faq'
import Sponsor from '~/components/sponsor'
import Agenda from '~/components/agenda'
import Tcd from '~/components/tcd/tcd'

export default {
  components: {
    Socialicon,
    Navbar,
    Home,
    About,
    Carousel,
    Voting,
    Faq,
    Sponsor,
    Agenda,
    Tcd
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
