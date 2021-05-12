<template>
  <div class="plan-action-container">
    <div>
      <h3 class="subtitle">
        Nos services
      </h3>
      <div class="cards-prestation">
        <card-prestation v-for="card in cards" :key="card.title" :title="card.title" :copy="card.description" :icon="card.icon" />
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
          description: 'Plateforme Web Développement CRM Modules spécifiques Webservices et API',
          icon: 'sitesurmesure'
        },
        site_vitrine: {
          title: 'Site vitrine',
          description: 'Solution sur-mesure Design professionnel Référencement Google Hébergement',
          icon: 'sitevitrine'
        },
        site_e_comerce: {
          title: 'Site e-commerce',
          description: 'Gestion des contenus Outils marketing 100% Propriétaire',
          icon: 'siteecommerce'
        },
        seo: {
          title: 'SEO',
          description: 'Référencement optimal de votre site Web et compatibilité accrue avec le robot Google.',
          icon: 'SEO'
        }
      }
    }
  }
}
</script>
<style>
.plan-action-container {
    display: flex;
    margin: 0 auto;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: rgb(0, 0, 0);
    background-color: #005f82b6;
    padding-top: 2rem;
    padding-bottom: 2rem;
  }
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
