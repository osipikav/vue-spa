<template>
  <div>
    <post-item v-for="post in posts" :post="post" />
  </div>
</template>

<script>
import PostItem from './PostItem.vue';
export default {
  components: {
    PostItem,
  },

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
