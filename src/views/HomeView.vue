<template>
	<div class="home">
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


      
        <vCatalogTop/>
      
    </section>
    
  </div>
	</div>
</template>

<script>
	// @ is an alias to /src
	import vCatalogTop from '../components/v-catalog-top.vue';
  import vCatalog from '../components/v-catalog.vue';
	export default {
		name: 'Home',
		components: {
      vCatalogTop,
      vCatalog
		},
    data() {
      return {
        title: 'Актуальное',
        title2: 'Популярная статья'
        
      }
    },
    
    
	}
</script>

<style scoped>

.row-flex {
  display: flex;
}

</style>