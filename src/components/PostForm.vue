<template>
  <div>
    <form @submit.prevent>
      <h3>post creation</h3>
      <input
        v-bind:value="title"
        @input="title = $event.target.value"
        type="text"
        placeholder="name"
      />
      <input
        v-bind:value="body"
        @input="body = $event.target.value"
        type="text"
        placeholder="description"
      />
      <button class="btn">create</button>
    </form>
  </div>
</template>

<script>
export default {};
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
