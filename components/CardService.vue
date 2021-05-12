<template>
  <div class="card-prestation">
    <div class="icon">
      <img :src="require(`~/assets/icons/${icon}.png`)" class="icon">
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
  name: 'CardPrestation',
  props: {
    title: { type: String, default: 'Card Title' },
    copy: { type: String, default: 'This is the card default description.' },
    icon: { type: String, default: 'CardPNG' }
  }
}
</script>
<style>
.card-prestation {
   width: 20vw;
   height: 20vh;
   background-color: #ffffffa1;
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
   height: 70px;
   max-width:80px;
   display: flex;
   justify-content: center;
   align-items: center;
   transition: all 0.8s ease;
   background-position: 0px;
}

.title-card-prestation {
  font-weight: bold;
  color: black;
}

.icon, .title-card-prestation {
  margin-top: 20px;
}

.card-prestation .card-prestation-text {
   width: 80%;
   margin: 0 auto;
   font-size: 13px;
   text-align: center;
   margin-top: 20px;
   color: rgb(0, 0, 0);
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
.card-prestation:hover .icon, .card-prestation-text {
  transition: all 0.3s ease;
  margin-top: 0px;
}
.card-prestation:hover:hover {
   height: 260px;
}
</style>
