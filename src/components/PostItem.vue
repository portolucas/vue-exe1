<template>
  <div class="post">
    <h1>{{ post.title }}</h1>
    <p>{{ post.content }}</p>
  </div>
</template>

<script>
export default {
  props: {
    post: Object,
  },
};
</script>

<style scoped>
.post {
  display: block;
  color: black;
}
</style>
