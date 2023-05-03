<template>
	<div class="mange">
		<Header msg="Welcome to Your Vue.js App" />
		<div class="container">
    <section class="py-5">
      
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

        <button class="btn btn-success" v-on:click.prevent="AddPost">Добавить статью</button>
      </form>
    </section>
  </div>
  <div class="mb-4 d-flex justify-content-between align-items-center">
        <h2>{{ title3 }}</h2>
      </div>
      <table class="table">
        <tr>
          <th>#</th>
          <th>Название</th>
          <th>Действия</th>
        </tr>
        <tr v-for="(post, index) in posts" :key="post.name">
          <td>{{ index + 1}}</td>
          <td>{{ post}}</td>
          <td>
            <button class="btn btn-sm btn-del" v-on:click="DelPost(index)">Удалить</button>
          </td>
        </tr>
      </table>
    </section>
    <div v-if="posts.length ===0">
        <h4 class="VIF">Нет постов, создай их.</h4>  
    </div> 
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
        title3: 'Управление статьями',
        placeholder: 'Придумайте название статьи',
        placeholder2: 'Напишите описание статьи',
        posts: [
         'Firste post', 'Two post'
        ],
        InputValue: '',
        InputValue2: '',
        editTask: null,
      }
    },
    methods: {
      InputFields(event) {
        this.InputValue = event.target.value
      },
      // InputFields2(event) {
      //   this.InputValue2 = event.target.value
      // },
      AddPost() {
        if(this.InputValue !== '') {
          this.posts.push(this.InputValue)
          this.InputValue = ''
        }
      },
      DelPost(index) {
        this.posts.splice(index, 1)
      },
    }
	}
</script>

<style scoped>

.btn-del {
  background-color: red;
  color: white;
}
.VIF {
  text-align: center;
}

</style>