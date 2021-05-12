<template>
  <div class="plan-action-container">
    <div>
      <h3 class="subtitle">
        Notre plan d'action
      </h3>
      <div class="cards-bandeau">
        <card-action v-for="card in cards" :key="card.title" :icon="card.icon" :title="card.title" />
      </div>
    </div>
  </div>
</template>
<script>
import CardAction from '~/components/CardAction.vue'
export default {
  components: { CardAction },
  data () {
    return {
      cards: {
        conception: {
          title: 'Conception',
          icon: 'conception'
        },
        planification: {
          title: 'Planification',
          icon: 'planification'
        },
        realisation: {
          title: 'Réalisation',
          icon: 'realisation'
        },
        livraison: {
          title: 'Livraison',
          icon: 'livraison'
        },
        accompagnement: {
          title: 'Accompagnement',
          icon: 'accompagnement'
        }
      }
    }
  }
}
</script>
<style>

</style>
