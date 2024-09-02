<template>
  <div class="content">
    <div class="header">
      <h1 class="title">Мой склад</h1>
      <button class="setting">
        <img src="../img/icons/settings.svg" alt="" />
        <p>Настройки отчёта</p>
      </button>
    </div>
    <Product />
    
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Product from "./Product.vue";


export default defineComponent({
  components: { Product},
  setup() {
    return {};
  },
});
</script>

<style scoped>
.content {
  margin: 24px 40px 40px 0px;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 24px;
}
.header {
  display: flex;
  justify-content: space-between;
  height: 40px;
}
.title {
  font-family: "Lato Semibold";
  font-size: 30px;
}
.setting {
  display: flex;
  gap: 4px;
  align-items: center;
  justify-content: center;
  width: 170px;
  border: 1px solid #d8dce9;
  background-color: #f4f5f8;
  border-radius: 4px;
}

.setting p {
  font-size: 14px;
  font-family: "Lato Regular";
}
</style>
