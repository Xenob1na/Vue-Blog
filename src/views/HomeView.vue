<template>
	<div class="home">
		<Header msg="Welcome to Your Vue.js App" />
		<div class="container">
    <section class="py-5">
      <div class="mb-4 d-flex justify-content-between align-items-center">
        <h2>Актуальное</h2>
        <RouterLink to="/allpost" ><button class="btn btn-sm btn-primary">Все статьи</button></RouterLink>
      </div>

      <div class="row">
        <div class="col-3">
          <div class="card">
            <img class="card-img-top" src="../assets/images/placeholder-blue.png" alt="placeholder">
            <div class="card-body">
              <p class="card-text">
                <small class="text-muted">09.04.2021 16:00</small>
              </p>

              <h5 class="card-title">Название статьи</h5>
              <p class="card-text">Описание статьи</p>

              <a href="#" class="btn btn-primary">Читать</a>
            </div>
          </div>
        </div>
        <div class="col-3">
          <div class="card">
            <img class="card-img-top" src="../assets/images/placeholder-blue.png" alt="placeholder">
            <div class="card-body">
              <p class="card-text">
                <small class="text-muted">08.04.2021 16:00</small>
              </p>

              <h5 class="card-title">Название статьи</h5>
              <p class="card-text">Описание статьи</p>

              <a href="#" class="btn btn-primary">Читать</a>
            </div>
          </div>
        </div>
        <div class="col-3">
          <div class="card">
            <img class="card-img-top" src="../assets/images/placeholder-blue.png" alt="placeholder">
            <div class="card-body">
              <p class="card-text">
                <small class="text-muted">07.04.2021 16:00</small>
              </p>

              <h5 class="card-title">Название статьи</h5>
              <p class="card-text">Описание статьи</p>

              <a href="#" class="btn btn-primary">Читать</a>
            </div>
          </div>
        </div>
        <div class="col-3">
          <div class="card">
            <img class="card-img-top" src="../assets/images/placeholder-blue.png" alt="placeholder">
            <div class="card-body">
              <p class="card-text">
                <small class="text-muted">06.04.2021 16:00</small>
              </p>

              <h5 class="card-title">Название статьи</h5>
              <p class="card-text">Описание статьи</p>

              <a href="#" class="btn btn-primary">Читать</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-5">
      <div class="mb-4 d-flex justify-content-between align-items-center">
        <h2>Случайная статья</h2>
      </div>


      <a href="#" class="card bg-dark text-white">
        <img class="card-img" src="../assets/images/placeholder-blue.png" alt="placeholder">
        <div class="card-img-overlay">
          <h5 class="card-title">Название статьи</h5>
        </div>
      </a>
    </section>
  </div>
	</div>
</template>

<script>
	// @ is an alias to /src
	import Header from '@/components/Header.vue'
	export default {
		name: 'Home',
		components: {
			Header,
		},
	}
</script>