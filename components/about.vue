<template>
  <div>
    <b-row class="animate__animated animate__fadeInLeft animate__delay-1.4s">
      <b-col col="12" lg="7">
        <h3>
          <b class="roboto-fat text-purple text-title">BarCamp Cyberjaya</b>
        </h3>
        <h4>
          <b class="roboto-fat text-purple">Share | Learn | Inspire</b>
        </h4>
        <h5 class="roboto-light text-purple text-justify mt-3" style="line-height:1.5em;">
          {{ aboutDesc }}
        </h5>
        <b-row class="mt-4 d-none d-sm-block">
          <b-col>
            <b-button
              href="https://forms.gle/bH4NuamofgKq4PXp9"
              target="_blank"
              variant="outline-light"
              size="lg"
              class="abt-btn p-2 mr-1"
              pill
            >
              Be a Speaker
            </b-button>
            <b-button
              href ="https://forms.gle/g3WQFXg1vW9vxGLy8"
              target="_blank"
              variant="outline-light"
              size="lg"
              class="abt-btn p-2 mr-1"
              pill
            >
              Be an Audience
            </b-button>
          </b-col>
        </b-row>
        <b-row class="mt-4 d-block d-sm-none">
          <b-col>
            <b-button
              href="https://forms.gle/bH4NuamofgKq4PXp9"
              target="_blank"
              variant="outline-light"
              size="md"
              class="abt-btn p-3 mr-1"
              pill
            >
              Be a Speaker
            </b-button>
            <b-button
              href ="mailto:itsociety.barcamp20@gmail.com"
              target="_blank"
              variant="outline-light"
              size="md"
              class="abt-btn p-3 mr-1"
              pill
            >
              Be a Sponsor
            </b-button>
          </b-col>
        </b-row>
      </b-col>
      <b-col col="12" lg="5" class="d-none d-md-block text-center">
        <b-img
          src="~/assets/img/barcamp-fire.png"
          style="width:auto; height:20em"
          fluid
        />
      </b-col>
    </b-row>
    <AboutCards />
    <AboutVid />
  </div>
</template>

<script>
import AboutCards from '~/components/about-card'
import AboutVid from '~/components/about-vid'

export default {
  components: {
    AboutCards,
    AboutVid
  },
  data: () => {
    return {
      aboutDesc: 'Barcamp Cyberjaya is an international network of user-generated conference that brings people together to share their passion around technology. There is no preset of speakers for BarCamp like usual conferences. Participants get to vote for speakers based on the topics proposed by speakers.'
    }
  }
}
</script>

<style scoped>
  .abt-btn {
    width:8.5em;
    color:white;
    border-color:rgb(108,48,130);
    background-color: rgb(108,48,130);
  }

  .abt-btn:hover {
    width:8.5em;
    color:rgb(108,48,130);
    border-color:rgb(108,48,130);
    background-color: white;
  }
</style>
