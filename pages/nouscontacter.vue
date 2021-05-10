<template>
  <div class="container">
    <div>
      <div>
        <h3 class="subtitle">
          Nous contacter
        </h3>
      </div>
      <div class="form-container">
        <contact-form />
      </div>
    </div>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm.vue'
export default {
  components: { ContactForm }

}
</script>
<style>
.form-container {
  position: relative;
  left: 10px;
}

@media screen and (min-width: 280px) {
  .form-container {
  position: relative;
  left: 5px;
}
}
@media screen and (min-width: 300px) {
  .form-container {
  position: relative;
  left: 0;
}
}
</style>
