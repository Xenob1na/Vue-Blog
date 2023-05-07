<template>
	<div class="about">
		<div class="container">
    <section class="py-5">
      <div class="mb-4 d-flex  align-items-baseline">
        <h2>Все статьи</h2>
      </div>
      <div class="row">
        <v-catalog-all/>
      </div>
    </section>
  </div>
	</div>
</template>

<script>
	// @ is an alias to /src
	
  import vCatalogAll from '../components/v-catalog-all.vue';
	export default {
		name: 'Home',
		components: {
      vCatalogAll
		},
	}
</script>

<style scoped>



</style>