<template>
  <div class="post">
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostForm from './components/PostForm.vue';
import PostList from './components/PostList.vue';

export default {
  components: {
    PostList,
    PostForm,
  },

  data() {
    return {
      posts: [
        { id: 1, title: 'title 1', body: 'description 1' },
        { id: 2, title: 'title 2', body: 'description 2' },
        { id: 3, title: 'title 3', body: 'description 3' },
        { id: 4, title: 'title 4', body: 'description 4' },
      ],
    };
  },

  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.post {
  display: flex;
  flex-direction: column;
  height: 300px;
}
</style>
