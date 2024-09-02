<template>
  <div class="header">
    <div class="header-item"><p>Товар</p></div>
    <div class="header-item">
      <p>
        Остаток на WB <img src="../img/icons/arrow-down.svg" alt="" />
        <img src="../img/icons/question.svg" alt="" />
      </p>
      <p>Остаток на складе<img src="../img/icons/arrow-down.svg" alt="" /></p>
    </div>
    <div class="header-item">
      <p>
        Остаток у поставщика<img src="../img/icons/arrow-down.svg" alt="" />
        <img src="../img/icons/question.svg" alt="" />
      </p>
      <p>Хватит на складе<img src="../img/icons/arrow-down.svg" alt="" /></p>
    </div>
    <div class="header-item">
      <p>
        Остаток мой склад<img src="../img/icons/arrow-down.svg" alt="" />
        <img src="../img/icons/question.svg" alt="" />
      </p>
      <p>Хватит на складе<img src="../img/icons/arrow-down.svg" alt="" /></p>
    </div>
    <div class="header-item">
      <p>Остаток всего<img src="../img/icons/arrow-down.svg" alt="" /></p>
      <p>Хватит на складе<img src="../img/icons/arrow-down.svg" alt="" /></p>
    </div>
    <div class="header-item">
      <p>
        В пути от производителя<img src="../img/icons/arrow-down.svg" alt="" />
        <img src="../img/icons/question.svg" alt="" />
      </p>
    </div>
    <div class="header-item">
      <p>Скорость заказов<img src="../img/icons/arrow-down.svg" alt="" /></p>
      <p>
        за <input type="text" value="7 дней" />
        <img src="../img/icons/question.svg" alt="" />
      </p>
    </div>
    <div class="header-item"><p>История изменения</p></div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    return {};
  },
});
</script>

<style scoped>
.header {
  width: 100%;

  background-color: #5068a5;
  border-radius: 4px;
  display: grid;
  grid-template-columns: 4fr 2fr 2fr 2fr 2fr 2fr 2fr 1fr;
  gap: 15px;
  padding: 0 5px;
}
.header-item {
  color: white;
  font-family: "Lato Regular";
  font-size: 13px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap: 5px;
}
p {
  display: flex;
  gap: 4px;
  align-items: center;
  justify-content: center;
}
img {
  width: 16px;
}
input {
  width: 49px;
  color: #5068a5;
  border-radius: 4px;
  border: #5068a5;
}
</style>
