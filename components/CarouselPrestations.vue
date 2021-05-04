<template>
  <div>
    <agile
      class="slides-container"
      :nav-button="false"
      :autoplay-speed="5000"
      :speed="2500"
      fade
      pause-on-hover
      pause-on-dots-hover
      autoplay
    >
      <div v-for="site in list_sites" :key="site.id" class="slide">
        <img class="img-showcase" :src="site.image_showcase">
        <h4>
          {{ site.title }}
        </h4>
        <p>
          {{ site.description }}
        </p>
        <template slot="prevButton" />
        <template slot="nextButton" />
      </div>
    </agile>
  </div>
</template>
<script>
import { VueAgile } from 'vue-agile'

export default {
  components: {
    agile: VueAgile
  },
  data () {
    return {
      list_sites: {
        alan_site: {
          title: 'Site C.V Alan GARBO',
          description: `Le site C.V d'Alan a été réalisé dans le cadre
                            de recheche de stage et alternance au début
                            de l'année 2021.`,
          image_showcase: '~/assets/img/alan_site_screen.png',
          btn: 'Accéder au site',
          link: 'https://alangarbo.com'
        },
        samuel_site: {
          title: 'Site C.V Samuel GALIERE',
          description: `Le site C.V de Samuel a été réalisé dans le cadre
                            de recheche de stage et alternance au début
                            de l'année 2021.`,
          image_showcase: '~/assets/img/alan2021.jpg',
          btn: 'Accéder au site',
          link: 'https://samuelgaliere.com'
        }
      }
    }
  }
}
</script>
<style>
.slides-container {
    width: 50vw;
    height: 50vw;
    padding-top: 3rem;
}
</style>
