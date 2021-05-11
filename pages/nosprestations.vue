<template>
  <div class="container">
    <div>
      <h3 class="subtitle">
        Nos préstations
      </h3>
      <div class="contains-text">
        <p>
          Nous vous proposons un suivi complet pour la mise en place d’un site Web OpenSource. <br> <br>
          Du maquettage à la mise en production et au suivi technique, nous vous proposons une large gamme de prestations complètes et complémentaires. <br> <br>
          Nous travaillons avec le framework NuxtJS qui simplifie et augmente considérablement les capacités du déjà très reconnu VueJS. <br><br>
          Fluidité, rapidité, qualité, optimisation (SEO, etc.) sont les lignes directrices de notre développement, avec l’utilisation d’outils de pointe pour un rendu qui maximisera votre visibilité et l’expérience de vos utilisateurs.
        </p>
      </div>
      <div class="cards-prestation">
        <card-prestation v-for="card in cards" :key="card.title" :title="card.title" :copy="card.description" />
      </div>
    </div>
  </div>
</template>
<script>
import CardPrestation from '~/components/CardPrestation.vue'
export default {
  components: { CardPrestation },
  data () {
    return {
      cards: {
        site_sur_mesure: {
          title: 'Site sur mesure',
          description: 'Plateforme Web Développement CRM Modules spécifiques Webservices et API'
        },
        site_vitrine: {
          title: 'Site vitrine',
          description: 'Solution sur-mesure Design professionnel Référencement Google Hébergement'
        },
        site_e_comerce: {
          title: 'Site e-commerce',
          description: 'Gestion des contenus Outils marketing 100% Propriétaire'
        },
        seo: {
          title: 'SEO',
          description: 'Référencement optimal de votre site Web et compatibilité accrue avec le robot Google.'
        }
      }
    }
  }
}
</script>
<style>
.cards-prestation {
   max-width: 1024px;
   width: 100%;
   padding: 0 4%;
   padding-top: 30px;
   margin: 0 auto;
   display: flex;
   justify-content: center;
   align-items: center;
}
</style>
