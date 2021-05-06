<template>
  <div class="carousel">
    <div v-for="site in list_sites" :key="site.name" class="container-site-card fade">
      <card-site
        :id="site.id"
        :title="site.title"
        :description="site.description"
        :button-link="site.link"
        :button-title="site.btn"
      />
      <a class="prev" @click="changeSlide(-1)">&#10094;</a>
      <a class="next" @click="changeSlide(1)">&#10095;</a>
    </div>
  </div>
</template>
<script>
import CardSite from './CardSite.vue'
export default {
  components: { CardSite },
  data () {
    return {
      slideIndex: 1,
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
  },
  mounted () {
    this.showSlides(this.slideIndex)
  },
  methods: {
    changeSlide (n) {
      this.showSlides(this.slideIndex += n)
    },
    currentSlide (n) {
      this.showSlides(this.slideIndex = n)
    },
    showSlides (n) {
      let i
      const slides = document.getElementsByClassName('container-site-card')
      if (n > slides.length) { this.slideIndex = 1 }
      if (n < 1) { this.slideIndex = slides.length }
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = 'none'
      }
      slides[this.slideIndex - 1].style.display = 'block'
    }
  }
}
</script>
<style>
* { box-sizing: border-box; }

.container-site-card {
  display: none;
}

.prev, .next {
  cursor: pointer;
  color: white;
  padding: 1rem;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

@media screen and (min-width: 768px) {
  .prev, .next {
    padding: 2rem;
  }
}
@media screen and (min-width: 1000px) {
  .prev, .next {
    padding: 3rem;
  }
}
@media screen and (min-width: 1350px) {
  .prev, .next {
    padding: 5rem;
  }
}

.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}

@keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}

#site_alan_garbo .card-component-site {
    background-image: url('~assets/img/alan_site_screen.png');
}

#site_samuel_galiere .card-component-site {
    background-image: url('~assets/img/samuel_site_screen.png');
}
</style>
