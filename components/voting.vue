<template>
  <b-container>
    <h4 class="mt-2">
      <b class="roboto-fat text-purple text-title">Voting Results of Proposed Talks</b>
    </h4>
    <b-button
      href="https://forms.gle/eT3SrzGJPM78MJsF9"
      target="_blank"
      variant="outline-light"
      size="lg"
      class="abt-btn p-3 mr-1 mt-2"
      pill
    >
      Vote for Talks
    </b-button>
    <iframe
      width="100%"
      height="399"
      seamless
      frameborder="0"
      scrolling="yes"
      fluid
      src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR-fQizF3gF6shYoqI24L0KTaQWWSd7gaEQlOn99uzBmFnbpWan95z0KnQhp6mc0zEqdkTVutjc6cDS/pubchart?oid=1619883027&amp;format=interactive"
      class="mt-2"
    >
    </iframe>
  </b-container>
</template>

<script>
export default {

}
</script>

<style>
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
