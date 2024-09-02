<template>
  <div class="container"><Sidebar /> <Content /></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Sidebar from "./components/Sidebar.vue";
import Content from "./components/Content.vue";

export default defineComponent({
  components: {
    Sidebar,
    Content
  },
  setup() {
    return {};
  },
});
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

.container {
  display: flex;
  gap: 40px;
  background-color: #f4f5f8;
}
</style>
