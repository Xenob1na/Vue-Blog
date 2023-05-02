<template>
	<div class="hello">
		<header class="bg-primary text-white py-2">
			<div class="container d-flex justify-content-between">
			<a href="#" class="navbar-brand text-white logo">Статейка</a>

			<nav class="nav">
				<RouterLink to="/" class="nav-link text-white">Главная</RouterLink>
        		<RouterLink to="/allpost" class="nav-link text-white">Все статьи</RouterLink>
				<RouterLink to="/managepost" class="nav-link text-white">Управление статьями</RouterLink>
			</nav>
			</div>
	    </header>
	</div>
</template>

<script>
	export default {
		name: 'HelloWorld',
		props: {
			msg: String,
		},
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	
	.logo {
		align-items: center;
		font-size: 25px;
	}
</style>
