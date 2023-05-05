<template>
    <div class='post'>
        <div class="container">
    <section class="py-5">
      <h2 class="mb-4">{{ film.name }}</h2>
       <!-- <img :src=" require('../assets/mocks/data.js' + film.image ) ">  -->

      <img class="mb-4 w-100" src="../assets/images/placeholder-blue.png" alt="placeholder">

      <p>
        {{ film.description }}
    </p>
        
    </section>
  </div>
    </div>
</template>

<script>
import data from '../mocks/data'
export default {
  data() {
    return {
        film: null
    }
  },
  created() {
    const film = data.find(film => film.id == this.$route.params.id)
    if (film) {
      this.film = film
    }
  }
}
</script>