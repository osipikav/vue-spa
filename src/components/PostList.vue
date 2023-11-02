<template>
  <div v-for="post in posts">
    <div class="post-item">
      {{ post.title }}
      {{ post.body }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.post-item {
  background-color: aqua;
  margin: 10px 0;
}
</style>
