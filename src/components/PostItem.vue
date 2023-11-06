<template>
  <div class="post-item">
    {{ post.title }}
    {{ post.body }}
    <my-button @click="DeletePost">delete</my-button>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
  methods: {
    DeletePost() {
      console.log('this.event.target');
    },
  },
};
</script>

<style scoped>
.post-item {
  background-color: aqua;
  margin: 10px 0;
}
button {
  margin: 5px;
}
</style>
