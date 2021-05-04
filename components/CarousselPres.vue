<template>
  <div class="contains-carousel">
    <section class="carousel">
      <ol class="carousel__viewport">
        <li
          v-for="site in list_sites"
          :id="site.name_in_page"
          :key="site.id"
          class="carousel-slide"
          :tabindex="site.index"
          :style="{backgroundImage: `url(${site.image_showcase})`}"
        >
          <div class="carousel-snapper">
            <h4 class="title_showcase">
              {{ site.title }}
            </h4>
            <p class="description_showcase">
              {{ site.description }}
            </p>
            <a :href="site.link"><button>{{ site.btn }}</button></a>
            <a href="" class="carousel-prev" />
            <a href="" class="carousel-next" />
          </div>
        </li>
      </ol>
    </section>
  </div>
</template>
<script>
export default {
  data () {
    return {
      list_sites: {
        alan_site: {
          title: 'Site C.V Alan GARBO',
          description: `Le site C.V d'Alan a été réalisé dans le cadre
                            de recheche de stage et alternance au début
                            de l'année 2021.`,
          image_showcase: 'https://cdn.pixabay.com/photo/2021/04/26/10/48/lake-6208614_960_720.jpg',
          btn: 'Accéder au site',
          link: 'https://alangarbo.com',
          name_in_page: 'showcase_1',
          index: 0
        },
        samuel_site: {
          title: 'Site C.V Samuel GALIERE',
          description: `Le site C.V de Samuel a été réalisé dans le cadre
                            de recheche de stage et alternance au début
                            de l'année 2021.`,
          image_showcase: 'assets/img/alan2021.jpg',
          btn: 'Accéder au site',
          link: 'https://samuelgaliere.com',
          name_in_page: 'showcase_2',
          index: 1
        }
      }
    }
  }
}
</script>
<style>
.contains-carousel {
    height: 70vh;
    width: 60vw;
}
.carousel-slide{
    list-style: none;
    background-size: cover;
    background-repeat: no-repeat;
}
</style>
