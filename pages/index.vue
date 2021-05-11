<template>
  <div>
    <div>
      <accueil id="accueil" />
      <nousdecouvrir id="nousdecouvrir" />
      <nosprestations id="nosprestations" />
      <nosprojets id="nosprojets" />
      <nouscontacter id="nouscontacter" />
    </div>
  </div>
</template>

<script>
import Accueil from './accueil.vue'
import Nousdecouvrir from './nousdecouvrir.vue'
import Nosprestations from './nosprestations.vue'
import Nouscontacter from './nouscontacter.vue'
import Nosprojets from './nosprojets.vue'

export default {
  components: { Accueil, Nousdecouvrir, Nosprestations, Nouscontacter, Nosprojets }
}
</script>

<style>

</style>
