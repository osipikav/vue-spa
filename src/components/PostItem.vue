<template>
  <div class="post-item">
    {{ post.title }}
    {{ post.body }}
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
};
</script>

<style scoped>
.post-item {
  background-color: aqua;
  margin: 10px 0;
}
</style>
