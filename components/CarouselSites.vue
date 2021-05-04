<template>
  <div class="carousel">
    <div v-for="site in list_sites" :key="site.name">
      <card-site
        :id="site.id"
        :title="site.title"
        :description="site.description"
        :button-link="site.link"
        :button-title="site.btn"
      />
    </div>
  </div>
</template>
<script>
import CardSite from './CardSite.vue'
export default {
  components: { CardSite },
  data () {
    return {
      list_sites: {
        alan_site: {
          id: 'site_alan_garbo',
          title: 'Site C.V Alan GARBO',
          description: `Le site C.V d'Alan a été réalisé dans le cadre
                            de recheche de stage et alternance au début
                            de l'année 2021.`,
          image_showcase: 'alan_site_screen.png',
          btn: 'Accéder au site',
          link: 'https://alangarbo.com'
        },
        samuel_site: {
          id: 'site_samuel_galiere',
          title: 'Site C.V Samuel GALIERE',
          description: `Le site C.V de Samuel a été réalisé dans le cadre
                            de recheche de stage et alternance au début
                            de l'année 2021.`,
          image_showcase: 'samuel_site_screen.png',
          btn: 'Accéder au site',
          link: 'https://samuelgaliere.com'
        }
      }
    }
  }
}
</script>
<style>
#site_alan_garbo .card-component-site {
    background-image: url('~assets/img/alan_site_screen.png');
}

#site_samuel_galiere .card-component-site {
    background-image: url('~assets/img/samuel_site_screen.png');
}
</style>
