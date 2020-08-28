<template>
  <b-container>
    <b-row>
      <b-col lg="8" md="12">
        <b-img src="~/assets/img/barcamp-agenda.png" fluid />
      </b-col>
      <b-col lg="4" md="12" class="mt-1">
        <h3>Webinar Links</h3>
        <div v-for="(webinar,i) in webinars" :key="`webinar-${i}`">
          <b-card :title="`Webinar ${webinar.number}`" class="mt-3 text-purple">
            <a :href="`${webinar.link}`" target="_blank" class="card-link">{{ webinar.link }}</a>
          </b-card>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  data: () => {
    return {
      webinars: [
        {
          number: 'Main',
          link: 'https://meet.google.com/vxz-prim-uwe'
        },
        {
          number: '1',
          link: 'https://meet.google.com/zvn-jrnn-sgm'
        },
        {
          number: '2',
          link: 'https://meet.google.com/zbt-vhgg-nzv'
        },
        {
          number: '3',
          link: 'https://meet.google.com/ree-ddnn-muj'
        },
        {
          number: '4',
          link: 'https://meet.google.com/qtp-tvbm-cwm'
        }
      ]
    }
  }
}
</script>
