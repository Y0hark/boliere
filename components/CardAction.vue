<template>
  <div>
    <div class="card-action">
      <div class="icon">
        <img :src="require(`~/assets/icons/${icon}.png`)" class="icon">
      </div>
      <p class="title-card-action">
        {{ title }}
      </p>
    </div>
    <span class="point" />
  </div>
</template>
<script>
export default {
  name: 'CardAction',
  props: {
    title: { type: String, default: 'Card Title' },
    icon: { type: String, default: 'CardPNG' }
  }
}
</script>
<style>
.card-action {
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

.point {
   content: "";
   background-color: white;
   display: block;
   width: 50px;
   height: 25px;
   border-radius: 100%;
   display: flex;
}

.icon {
   margin: 0 auto;
   width: 100%;
   height: 68px;
   max-width:80px;
   display: flex;
   justify-content: center;
   align-items: center;
   transition: all 0.8s ease;
   background-position: 0px;
}

.title-card-action {
  font-weight: bold;
  color: black;
}

.icon, .title-card-action {
  margin-top: 25px;
}
</style>
