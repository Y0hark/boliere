<template>
  <div class="container">
    <div>
      <div>
        <h3 class="subtitle">
          Nous sommes
        </h3>
      </div>
      <div class="card-container">
        <div class="facecard">
          <card-personne-component id="alan" :name="nala.name" :description="nala.description" :button-name="nala.button" />
        </div>
        <div class="vertical_line" />
        <div class="facecard">
          <card-personne-component id="sammy" :name="sammy.name" :description="sammy.description" :button-name="sammy.button" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import CardPersonneComponent from '~/components/CardPersonneComponent.vue'
export default {
  components: { CardPersonneComponent },
  data () {
    return {
      nala: {
        name: 'Alan',
        description: 'Salut c\'est Alan ! Je suis moi et j\'aime bien le sexe !',
        button: 'Le CV d\'Alan'
      },
      sammy: {
        name: 'Samuel',
        description: 'Salut c\'est Samuel ! J\'ce que moi non!',
        button: 'Le CV de Sammy'
      }
    }
  }
}
</script>
<style>
    .facecard {
      width: 100%;
    }
    .vertical_line {
      display: none;
    }
    #alan .card-component {
      background-image: url('~assets/img/alan2021.jpg');
    }
    #sammy .card-component {
      background-image: url('~assets/img/samuel_pic.jpeg');
    }

    @media screen and (min-width: 768px) {
    .card-container {
      display: flex;
    }
    .facecard {
      width: 100%;
    }
    .vertical_line {
      display: block;
      border-right: 3px solid #005F82;
      height: 70vh;
    }
    #alan .card-content {
      margin-right: 2rem;
    }
    #sammy .card-content {
      margin-left: 2rem;
    }
    }

  @media screen and (min-width: 850px) {
    #alan .card-content {
      margin-right: 1rem;
    }
    #sammy .card-content {
      margin-left: 1rem;
    }
  }

  @media screen and (min-width: 1000px) {
    #alan .card-content {
      margin-right: 2rem;
    }
    #sammy .card-content {
      margin-left: 2rem;
    }
  }

  @media screen and (min-width: 1150px) {
    #alan .page-content {
      margin-right: 3rem;
    }
    #sammy .page-content {
      margin-left: 3rem;
    }
  }

  @media screen and (min-width: 1380px) {
    #alan .page-content {
      margin-right: 4rem;
    }
    #sammy .page-content {
      margin-left: 4rem;
    }
  }
</style>
