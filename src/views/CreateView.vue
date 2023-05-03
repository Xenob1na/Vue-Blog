<template>
	<div class="creat">
		<Header msg="Welcome to Your Vue.js App" />
		<div class="container">
    <section class="py-5">
      <div class="mb-4 d-flex justify-content-between align-items-center">
        <h2>Добавление статьи</h2>
      </div>

      <form>

        <div class="mb-3">
          <label>Название</label>
          <input type="text" class="form-control" 
          :placeholder="placeholder"
          :value="InputValue"
          v-on:input="InputFields"
          >
        </div>
        <div class="mb-3">
          <label>Описание</label>
          <textarea class="form-control" 
          :placeholder="placeholder2" 
          :value="InputValue2"
          v-on:input="InputFields2"
          rows="5"></textarea>
        </div>

        <button class="btn btn-success">Добавить статью</button>
      </form>
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
    data() {
      return {
        placeholder: 'Придумайте название статьи',
        placeholder2: 'Напишите описание статьи',
        posts: [
          {
            name: 'Post1',
            datetime: new Date().toLocaleTimeString()
          },
          {
            name: 'Post2',
            datetime: new Date().toLocaleTimeString()
          }
        ],
        InputValue: '',
        InputValue2: '',
      }
    },
    methods: {
      InputFields(event) {
        this.InputValue = event.target.value
      },
      InputFields2(event) {
        this.InputValue2 = event.target.value
      },
    }
	}
</script>