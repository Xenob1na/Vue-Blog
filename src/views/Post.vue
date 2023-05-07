<template>
    <div class='post'>
      <div class="container">
        <section class="py-5">
          <h2 class="mb-4">{{ post.name }}</h2>
          <img class="mb-4 w-100" src="../assets/images/placeholder-blue.png" alt="placeholder">
          <p>
            {{ post.description }}
         </p>
        </section>
    </div>
    <section class="comment">
      <v-comment/>
    </section>
  </div>
</template>

<script>
import vComment from '../components/v-comment.vue'
import data from '../mocks/data'
export default {
  data() {
    return {
        post: null
    }
  },
  created() {
    const post = data.find(post => post.id == this.$route.params.id)
    if (post) {
      this.post = post
    }
  },
  components: {
    vComment,
  }
}
</script>