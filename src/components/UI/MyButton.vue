<template>
  <button class="btn"><slot></slot></button>
</template>

<script>
export default {
  name: 'my-button',
};
</script>

<style scoped>
.btn {
  background-color: brown;
  /* width: 40px;
  height: 20px; */
}
</style>
