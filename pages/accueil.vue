<template>
  <div class="background_image container-accueil">
    <div>
      <h1 class="title">
        Bolière
      </h1>

      <h3 class="subtitle">
        Agence Web @Marseille
      </h3>

      <animated-links-exp />
    </div>
  </div>
</template>
<script>
import AnimatedLinksExp from '~/components/AnimatedLinksExp.vue'
export default {
  components: { AnimatedLinksExp }

}
</script>
<style>
.container-accueil {
  display: flex;
  margin: 0 auto;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
}
.background_image{
    background-image: url('~assets/img/bg_raw.jpg');
    background-attachment: fixed;
    background-size: cover;
    background-repeat: no-repeat;
    height: 100vh;
    width: 100vw;
}
</style>
