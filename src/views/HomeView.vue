<template>
  <page-menu />
  <search-bar />
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
