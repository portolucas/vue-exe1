<template>
  <div>
    <h1>Sidebar</h1>
    <ul>
      <li v-for="item in items" v-bind:key="item.title">
        <SidebarItems :items="item" />
      </li>
    </ul>
  </div>
</template>

<script>
import SidebarItems from "./SidebarItems";

export default {
  components: {
    SidebarItems,
  },
  props: {
    items: Array,
  },
};
</script>

<style scoped>
h1 {
color: black;
}
li {
  padding: 10px;
}
ul {
  margin-top: 30px;
}
</style>
