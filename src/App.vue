<template>
  <div id="app">
    <Header title="First Vue App" :menus="listMenus" />
    <div class="content">
      <Posts :posts="posts" />
      <Sidebar :items="sidebarItems" />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Posts from "./components/Posts";
import Sidebar from "./components/Sidebar";

export default {
  name: "App",
  components: {
    Header,
    Posts,
    Sidebar
  },
  data() {
    return {
      listMenus: [
        { title: "Home", link: this.getUrl() },
        { title: "Artigos", link: this.getUrl() + "/artigos" },
      ],
      posts: [
        { title: "Post 1", content: "Text 1" },
        { title: "Post 2", content: "Text 2" },
        { title: "Post 3", content: "Text 3" },
        { title: "Post 4", content: "Text 4s" },
      ],
      sidebarItems: [
        { title: "Item 1"},
        { title: "Item 2"},
        { title: "Item 3"},
        { title: "Item 4"},
      ],
    };
  },
  methods: {
    getUrl() {
      var url = window.location.protocol + "//" + window.location.host;
      return url;
    },
  },
};
</script>

<style>
#app {
  margin: 0;
  padding: 0;
  list-style: none;
  font-size: 1.2rem;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
}
.content {
  display: grid;
  grid-template-columns: 1fr 200px;
  grid-gap: 20px;
  max-width: 800px;
  padding: 10px;
  margin: 0 auto;
}
</style>
