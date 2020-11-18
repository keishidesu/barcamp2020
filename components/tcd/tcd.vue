<template>
  <div class="bg-tcd shiny">
    <b-container>
      <b-jumbotron class="d-none d-md-block bg-none animate__animated animate__fadeInLeft">
        <b-row>
          <b-col cols="5">
            <b-img src="~/assets/img/tcd-logo-small.png" fluid />
          </b-col>
          <b-col cols="7" class="text-center">
            <div style="color: #f2f20d; text-shadow: 3px 4px #1f2e2e;">
              <p style="letter-spacing: 5px; font-size: 3.5rem">COMING THIS</p>
              <p style="letter-spacing: 7px; font-size: 4rem">JANUARY 2021</p>
            </div>
            <b-button
              href="https://techcareerdays.com/"
              target="_blank"
              variant="light"
              size="lg"
              style="width:12em"
              pill
            >
              Learn More
            </b-button>
          </b-col>
        </b-row>
      </b-jumbotron>

      <b-jumbotron class="d-md-none bg-none animate__animated animate__fadeInLeft text-center">
        <b-img src="~/assets/img/tcd-logo-small.png" fluid />
        <div style="color: #f2f20d; text-shadow: 3px 4px #1f2e2e;">
          <p style="letter-spacing: 5px; font-size: 2.5rem">COMING THIS JANUARY 2021</p>
        </div>
        <b-button
          href="https://techcareerdays.com/"
          target="_blank"
          variant="light"
          size="lg"
          style="width:12em"
          pill
        >
          Learn More
        </b-button>
      </b-jumbotron>
    </b-container>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
/* .bg-tcd {
  background-image: linear-gradient(to right, #051C41 , #0099cc);
} */

.shiny {
  background-image: -webkit-linear-gradient(left, #051C41 25%, #004d99 37.5%, #248f8f, #004d99 62.5%, #051C41 75%);
  background-image: linear-gradient(90deg, #051C41 25%, #004d99 37.5%, #248f8f, #004d99 62.5%, #051C41 75%);
  background-position: right center;
  background-size: 400% auto;
}

.shiny:hover {
  background-position: left center;
  transition: background-position 2000ms ease-out;
}
</style>
