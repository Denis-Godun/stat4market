<template>
  
  <div class="size-list">
    <h3><img src="../img/icons/measuringtape.svg" alt="" />Размерный ряд</h3>
    <div class="list-header">
      <p class="header-name">Размер</p>
      <p class="header-name">Остаток на WB</p>
      <p class="header-name">Хватит на</p>
      <p class="header-name">Остаток у поставщика</p>
      <p class="header-name">Хватит на</p>
      <p class="header-name">Остаток мой склад</p>
      <p class="header-name">Хватит на</p>
      <p class="header-name">Остаток всего</p>
      <p class="header-name">Хватит на</p>
      <p class="header-name">В пути от производителя</p>
      <p class="header-name">Скорость заказов</p>
      <p class="header-name">История изменения</p>
    </div>
    <SizeItem /><SizeItem /><SizeItem /><SizeItem /><SizeItem /><SizeItem />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SizeItem from "./SizeItem.vue";

export default defineComponent({
  components: { SizeItem },
  setup() {
    return {};
  },
});
</script>

<style scoped>
.size-list {
  background-color: #f8f8f8;
  display: flex;
  flex-direction: column;

  border-left: 4px solid #a5d274;
  margin: 0 20px 10px 20px;
}
h3 {
  display: flex;
  align-items: center;
  gap: 15px;
  height: 48px;
  padding-left: 24px;
}
.list-header {
  font-family: "Lato Regular";
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  color: #999999;
  font-size: 12px;
  gap: 15px;
  padding: 0 24px;
}
.list-header p {
  text-decoration: none;
}
</style>
