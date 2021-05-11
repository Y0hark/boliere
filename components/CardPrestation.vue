<template>
  <div class="card-prestation">
    <div class="icon">
      <img src="~assets/icons/site_sur_mesure.svg">
    </div>
    <p class="title-card-prestation">
      {{ title }}
    </p>
    <p class="card-prestation-text">
      {{ copy }}
    </p>
  </div>
</template>
<script>
export default {
  props: {
    title: { type: String, default: 'Card Title' },
    copy: { type: String, default: 'This is the card default description.' }
  }
}
</script>
<style>
.card-prestation {
   width: 20vw;
   height: 20vh;
   background-color: #292929;
   margin: 10px;
   border-radius: 10px;
   box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.24);
   border: 2px solid rgba(7, 7, 7, 0.12);
   font-size: 16px;
   transition: all 0.3s ease;
   position: relative;
   display: inline-block;
   justify-content: center;
   align-items: center;
   flex-direction: column;
   cursor: pointer;
   transition: all 0.3s ease;
}

.icon {
   margin: 0 auto;
   width: 100%;
   height: 80px;
   max-width:80px;
   background: linear-gradient(90deg, #3d88a3b6 0%, #005f82b6 40%, rgba(0, 0, 0, 0.28) 60%);
   border-radius: 100%;
   display: flex;
   justify-content: center;
   align-items: center;
   color: white;
   transition: all 0.8s ease;
   background-position: 0px;
   background-size: 200px;
}

.card-prestation .card-prestation-text {
   width: 80%;
   margin: 0 auto;
   font-size: 13px;
   text-align: center;
   margin-top: 20px;
   color: white;
   font-weight: 200;
   letter-spacing: 2px;
   opacity: 0;
   max-height:0;
   transition: all 0.3s ease;
}

.card-prestation:hover .card-prestation-text {
   transition: all 0.3s ease;
   opacity: 1;
   max-height:40px;
}

.card-prestation:hover .icon {
   background-position: -120px;
   transition: all 0.3s ease;
}

.card-prestation:hover .icon i {
   background: linear-gradient(90deg, #3d88a3b6, #005f82b6);
   opacity: 1;
   transition: all 0.3s ease;
}

.card-prestation:hover:hover {
   height: 270px;
}
</style>
