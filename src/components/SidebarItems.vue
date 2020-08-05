<template>
  <div class="sidebar">
    <li>{{ items.title }}</li>
  </div>
</template>

<script>
export default {
  props: {
    items: Object,
  },
};
</script>

<style scoped>
.sidebar > div {
  margin-bottom: 10px;
  color: black;
}
li {
  color: black;
}

</style>
