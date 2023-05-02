<template>
	<div class="mange">
		<Header msg="Welcome to Your Vue.js App" />
		<div class="container">
    <section class="py-5">
      <div class="mb-4 d-flex justify-content-between align-items-center">
        <h2>Управление статьями</h2>
        <RouterLink to="/createpost" ><button class="btn btn-sm btn-success">Добавить статью</button></RouterLink>
      </div>

      <table class="table">
        <tr>
          <th>#</th>
          <th>Название</th>
          <th>Дата и время</th>
          <th>Действия</th>
        </tr>
        <tr>
          <td>1</td>
          <td>Статья 1</td>
          <td>09.04.2021 16:00</td>
          <td>
            <button class="btn btn-primary btn-sm">Редактировать</button>
            <button class="btn btn-danger btn-sm">Удалить</button>
          </td>
        </tr>
      </table>
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