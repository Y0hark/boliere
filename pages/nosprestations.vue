<template>
  <div class="container carousel-container">
    <div class="prestations">
      <h3>
        Nos préstations
      </h3>
    </div>
    <div class="contains-text">
      <p>
        Nous vous accompagnons dans le développement de site web spécifique avec des outils de pointe comme le framework Vue.JS ou Nuxt.JS.
        Commançant par la phase d’audit de l’existant, la rédaction de votre cahier des charges, jusqu’à l’optimisation
        du référencement naturel (SEO) de votre site pour préserver votre visibilité et développer vos ventes.
      </p>
    </div>
    <div class="carousel">
      <carousel-sites />
    </div>
  </div>
</template>
<script>
import CarouselSites from '~/components/CarouselSites.vue'
export default {
  components: { CarouselSites }
}
</script>
<style>
.carousel {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding-top: 3rem;
}

.carousel-container {
  display: block;
}

.prestations {
  padding-bottom: 2rem;
}
</style>
