<template>
  <section id="section4" class="d-flex flex-column justify-content-center bg-lighter" style="min-height: 80vh">
    <b-container class="text-center py-5" container-fluid>
      <b-row align-h="center">
        <b-col md="8" sm="10" align-self="center">
          <h1 class="mb-3">{{ section4.title[0].text }}</h1>
          <h2 class="mb-5">{{ section4.subtitle[0].text }}</h2>
          <video controls>
              <source :src="section4.video.url" type="video/mp4">
              Sorry, your browser doesn't support embedded videos.
          </video>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script>
export default {
  name: 'Section4',
  components: {
  },
  props: ['viewportDimensions'],
  data () {
    return {
    }
  },
  computed: {
    section4 () {
      const content = this.$store.getters['contentStore/getHomepage']
      return content.section4[0]
    }
  }
}
</script>

<style scoped>
  h1 {
    text-transform: none;
  }
  video {
    width: 100%;
  }
  video::-webkit-media-controls-fullscreen-button
  {
    display: none !important;
  }
</style>
