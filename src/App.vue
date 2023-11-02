<template>
  <div class="post">
    <post-form />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostForm from './components/PostForm.vue';
import PostList from './components/PostList.vue';
export default {
  components: { PostList, PostForm },
  data() {
    return {
      posts: [
        { id: 1, title: 'title 1', body: 'description 1' },
        { id: 2, title: 'title 2', body: 'description 2' },
      ],
      title: '',
      body: '',
    };
  },
  methods: {
    CreatePost() {
      const newPost = {
        id: Date.now,
        title: this.title,
        body: this.body,
      };
      this.posts.push(newPost);
      this.title = '';
      this.body = '';
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
