<!-- eslint-disable prettier/prettier -->
<template>
  <page-menu />
  <search-bar />
  <h4>纪  念  馆</h4>
  <celebraty-memory />
</template>

<script>
// @ is an alias to /src
import PageMenu from "@/components/PageMenu.vue";
import SearchBar from "@/components/SearchBar.vue";
import CelebratyMemory from "@/components/CelebratyMemory.vue";

export default {
  name: "HomeView",
  components: {
    PageMenu,
    SearchBar,
    CelebratyMemory,
  },
};
</script>
<style scoped>
h4 {
  font-family: text;
  position: absolute;
  top: 33%;
  width: 100%;
  text-align: center;
}
</style>
