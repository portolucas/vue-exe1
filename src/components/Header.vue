<template>
  <div class="header">
    <h1>{{ title }}</h1>
    <ul id="menu">
      <li v-for="menu in menus" :key="menu.title">
        <a :href="menu.link"> {{ menu.title }} </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String,
    menus: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background: #1d1e20;
}
h1 {
  display: flex;
  padding: 5px;
  margin: 0;
}
a {
  color: white;
}
#menu {
  display: flex;
}
li {
  margin-left: 10px;
  list-style-type: none;
  text-decoration: none;
  color: white;
}
</style>
