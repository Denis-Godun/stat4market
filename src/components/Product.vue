<template>
  <div class="products-container">
    <h2 class="title">Товары: <span>134 шт.</span></h2>
    <div class="table">
      <TableHeader />
      <ProductItems />
      <ProductItems />
      <ProductItems />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TableHeader from "./Table-header.vue";
import ProductItems from "./Product-items.vue";

export default defineComponent({
  components: { TableHeader, ProductItems },
  setup() {
    return {};
  },
});
</script>

<style scoped>
.products-container {
  background-color: white;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  gap: 24px;
}
.title {
  margin-left: 30px;
  margin-top: 30px;
  font-family: "Lato Semibold";
  font-size: 18px;
}
.title span {
  color: #ea5dbb;
}
.table {
  margin-left: 30px;
  margin-right: 30px;
  margin: 0 30px 30px 30px;
  height: 100%;
  display: flex;
  flex-direction: column;
  gap: 16px;
}
</style>
