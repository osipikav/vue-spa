<template>
  <form @submit.prevent>
    <h3>post creation</h3>
    <my-input v-model="post.title" type="text" placeholder="name" />
    <my-input v-model="post.body" type="text" placeholder="description" />
    <my-button class="btn" @click="CreatePost">create</my-button>
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
      this.post = {
        title: '',
        body: '',
      };
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}
</style>
