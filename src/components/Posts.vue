<template>
  <ul>
    <li v-for="post in posts" v-bind:key="post.content">
      <PostItem :post="post" />
    </li>
  </ul>
</template>

<script>
import PostItem from "./PostItem";

export default {
  components: {
    PostItem,
  },
  props: {
    posts: Array,
  },
};
</script>

<style scoped>
    


</style>