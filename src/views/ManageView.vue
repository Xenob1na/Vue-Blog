<template>
	<div class="mange">
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
          v-model="InputValue"
          >
        </div>
        <div class="mb-3">
          <label>Описание</label>
          <textarea class="form-control" 
          :placeholder="placeholder2" 
          v-model="InputValue2"
          rows="5"></textarea>
        </div>

        <button class="btn btn-success" id="liveToastBtn" v-on:click.prevent="AddPost">Добавить статью</button>
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
          <th>Дата</th>
          <th>Действия</th>
        </tr>
        <tr v-for="(post, index) in posts" :key="post.name">
          <td>{{ index + 1}}</td>
          <td>{{ post.title }}<br></td>
          <td>{{ post.date }}</td>
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
  
	
	export default {
		name: 'Home',
		components: {
	
      
		},
    data() {
      return {
        title3: 'Управление статьями',
        placeholder: 'Придумайте название статьи',
        placeholder2: 'Напишите описание статьи',
        posts: [
                {
                    title: 'Значимость проблем',
                    // description: 'Не следует, однако забывать, что консультация с широким активом влечет за собой процесс внедрения',
                    date: new Date().toLocaleDateString('RU'),
                },
                {
                    title: 'Формирование позиции',
                    // description: 'Не следует, однако забывать, что консультация с широким активом влечет за собой процесс внедрения!',
                    date: new Date().toLocaleDateString('RU'),
                },
            ],
        InputValue: '',
        InputValue2: '',
        editTask: null,
      }
    },
    methods: {

      AddPost() {
        if( this.InputValue !== '') {
                this.posts.push({
                title: this.InputValue,
                description: this.InputValue2,
                date: new Date().toLocaleTimeString(),
                }),
                this.InputValue = '',
                this.InputValue2 = ''
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