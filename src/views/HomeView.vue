<template>
	<div class="home">
		<Header msg="Welcome to Your Vue.js App" />
		<div class="container">
    <section class="py-5">
      <div class="mb-4 d-flex justify-content-between align-items-center">
        <h2>{{title}}</h2>
        <RouterLink to="/allpost" ><button class="btn btn-sm btn-primary">Все статьи</button></RouterLink>
      </div>

      <v-catalog/>
        
          
    </section>

    <section class="py-5">
      <div class="mb-4 d-flex justify-content-between align-items-center">
        <h2>{{ title2 }}</h2>
      </div>


      <a href="#" class="card bg-dark text-white">
        <img class="card-img" src="../assets/images/placeholder-blue.png" alt="placeholder">
        <div class="card-img-overlay">
          <h5 class="card-title">Формирование позиции</h5>
        </div>
      </a>
    </section>
    
  </div>
	</div>
</template>

<script>
	// @ is an alias to /src
	import Header from '@/components/Header.vue'
  import vCatalog from '../components/v-catalog.vue';
	export default {
		name: 'Home',
		components: {
			Header,
      vCatalog
		},
    data() {
      return {
        title: 'Актуальное',
        title2: 'Случайная статья'
        
      }
    },
    
    
	}
</script>

<style scoped>

.row-flex {
  display: flex;
}

</style>