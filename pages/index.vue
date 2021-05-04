<template>
  <div class="container">
    <div>
      <accueil id="accueil" />
      <nousdecouvrir id="nousdecouvrir" />
      <nosprestations id="nosprestations" />
      <nouscontacter id="nouscontacter" />
    </div>
  </div>
</template>

<script>
import Accueil from './accueil.vue'
import Nousdecouvrir from './nousdecouvrir.vue'
import Nosprestations from './nosprestations.vue'
import Nouscontacter from './nouscontacter.vue'

export default {
  components: { Accueil, Nousdecouvrir, Nosprestations, Nouscontacter }
}
</script>

<style>

</style>
