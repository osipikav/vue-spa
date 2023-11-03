<template>
  <form @submit.prevent>
    <h3>post creation</h3>
    <input v-model="post.title" type="text" placeholder="name" />
    <input v-model="post.body" type="text" placeholder="description" />
    <button class="btn" @click="CreatePost">create</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: '',
      },
    };
  },
  methods: {
    CreatePost() {
      this.post.id = Date.now();
      this.$emit('create', this.post);
      this.title = '';
      this.body = '';
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}
.btn {
  background-color: brown;
}
</style>
