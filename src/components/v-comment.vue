<template>
    <div class="container">
      <h3 class="mb-5">Оставить комментарий</h3>
        <div class="mb-3">
            <label for="exampleFormControlInput1" class="form-label">{{ labelName }}</label>
            <input type="text" class="form-control" id="exampleFormControlInput1" 
            v-model="InputValue"
            :placeholder="placeholderName">
            </div>
            <div class="mb-3">
            <label for="exampleFormControlTextarea1" class="form-label">{{ labelText }}</label>
            <textarea class="form-control" 
            v-model="InputValue2"
            id="exampleFormControlTextarea1" rows="3"></textarea>
            <button
            type="reset"
            class="btn btn-primary mt-4"
            v-on:click="AddComment"
            >Добавить</button>
        </div>
        <hr>
        <div>
            <h3>{{ h3Сomment }}</h3>
            <p class="col">Количество {{ AllComment.length }}</p>
        </div>
        <hr>
        <div class="card mb-4" v-for="(comment, index) in AllComment" :key="index">
          <div class="card-body">
            <p>{{ comment.comments }}</p>

            <div class="d-flex justify-content-between">
              <div class="d-flex flex-row align-items-center">
                <img src="https://mdbcdn.b-cdn.net/img/Photos/Avatars/img%20(4).webp" alt="avatar" width="25"
                  height="25" />
                <p class="small mb-0 ms-2">{{ comment.name }}</p>
              </div>
              <div class="d-flex flex-row align-items-center">
                <p class="small text-muted mb-0">{{ comment.date }}</p>
              </div>
            </div>
          </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'v-comment',
    data() {
        return {
            placeholderName: 'Ваше имя',
            labelName: 'Введите имя',
            labelText: 'Введите ваш комментарий',
            h3Сomment: 'Комментарии',
            AllComment: [
                {
                    name: 'Danil',
                    comments: 'Good Post!',
                    date: new Date().toLocaleTimeString(),
                },
                {
                    name: 'Anton',
                    comments: 'Good!',
                    date: new Date().toLocaleTimeString(),
                },
            ],
            InputValue: '',
            InputValue2: '',
        }
    },
    methods: {
        AddComment() {
            if( this.InputValue !== '') {
                this.AllComment.push({
                name: this.InputValue,
                comments: this.InputValue2,
                date: new Date().toLocaleTimeString(),
                }),
                this.InputValue = '',
                this.InputValue2 = ''
            }
        }
    }
}
</script>


<style>
    .col {
        margin: 0;
    }
</style>