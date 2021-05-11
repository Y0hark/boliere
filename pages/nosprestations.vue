<template>
  <div class="container carousel-container">
    <div>
      <h3 class="subtitle">
        Nos préstations
      </h3>
    </div>
    <div class="contains-text">
      <p>
        Nous vous proposons un suivi complet pour la mise en place d’un site Web OpenSource. <br> <br>
        Du maquettage à la mise en production et au suivi technique, nous vous proposons une large gamme de prestations complètes et complémentaires. <br> <br>
        Nous travaillons avec le framework NuxtJS qui simplifie et augmente considérablement les capacités du déjà très reconnu VueJS. <br><br>
        Fluidité, rapidité, qualité, optimisation (SEO, etc.) sont les lignes directrices de notre développement, avec l’utilisation d’outils de pointe pour un rendu qui maximisera votre visibilité et l’expérience de vos utilisateurs.
      </p>
    </div>
    <div class="projects">
      <h4>Nos projets</h4>
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
  padding-top: 1rem;
}

.carousel-container {
  display: block;
}

.projects {
  padding-top: 2rem;
}
</style>
