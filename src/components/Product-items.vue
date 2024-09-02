<template>
  <div class="products">
    <div class="item">
      <div class="item-product">
        <img src="../img/img.png" alt="" class="rose" />
        <div class="product-text">
          <a href="#" class="info"
            >Долговечный букет из 9 роз в коробке, в подарок — вечные
            стабилизированные цветы...</a
          >
          <p class="article">Артикул WB : 9619790</p>
        </div>
        <button><img src="../img/icons/link.svg" alt="" /></button
        ><button><img src="../img/icons/info.svg" alt="" /></button>
      </div>
      <div class="item-column">
        <EditableQuantityButton v-model:value="quantities['item1']" />
        <p class="before-date">Хватит на 549 дн</p>
      </div>
      <div class="item-column">
        <p class="static">1 000 шт.</p>
        <p class="before-date">Хватит на 549 дн</p>
      </div>
      <div class="item-column">
        <EditableQuantityButton v-model:value="quantities['item2']" />
        <p class="before-date">Хватит на 549 дн</p>
      </div>
      <div class="item-column">
        <p class="static">142 412 шт.</p>
        <p class="before-date">Хватит на 549 дн</p>
      </div>
      <div class="item-column">
        <EditableQuantityButton v-model:value="quantities['item3']" />
      </div>
      <div class="item-column">
        <EditableQuantityButton v-model:value="quantities['item4']" />
        <p class="before-date">150 шт. / 30 дней</p>
      </div>
      <div class="item-column"><button class="watch">Посмотреть</button></div>
    </div>

    <div class="">
      <button @click="toggleComponent" class="size">
        Размерный ряд <img src="../img/icons/2 arrow.svg" alt="" />
      </button>
      <transition name="fade">
        <SizeList v-if="showComponent" />
      </transition>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import SizeList from "./SizeList.vue";

import EditableQuantityButton from "./EditableQuantityButton.vue";

export default defineComponent({
  components: { SizeList, EditableQuantityButton },
  setup() {
    // Создаем переменную состояния для управления видимостью компонента
    const showComponent = ref<boolean>(false);

    // Метод для переключения видимости компонента
    const toggleComponent = () => {
      showComponent.value = !showComponent.value;
    };
    const quantities = ref({
      item1: "55 475 шт.",
      item2: "55 475 шт.",
      item3: "453 шт",
      item4: "5 шт/день",
    });
    return { quantities, showComponent, toggleComponent };
  },
});
</script>

<style scoped>
.products {
  font-family: "Lato Regular";
  border: 1px solid #d8dce9;
  width: 100%;
  border-radius: 4px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.item {
  display: grid;

  grid-template-columns: 4fr 2fr 2fr 2fr 2fr 2fr 2fr 1fr;
  gap: 15px;
  padding: 0 5px;
}
.item-product {
  display: flex;
  align-items: center;
  justify-content: space-around;
  gap: 5px;
}
.item-column {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 10px;
}

.before-date {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 12px;
  background: #f8f8f8;
  padding: 5px, 16px, 5px, 16px;
  height: 30px;
  border-radius: 4px;
}
.watch {
  background-color: #5068a5;
  border-radius: 4px;
  width: 84px;
  height: 24px;
  color: white;
  border: none;
  font-size: 12px;
}
.info {
  text-decoration: none;
  font-size: 13px;
  color: #5068a5;
}
.article {
  font-size: 12px;
  color: #666666;
}
.item-product button {
  background-color: white;
  border: none;
}
.static {
  margin-bottom: 10px;
  font-size: 14px;
}
.size {
  display: flex;
  background-color: white;
  border: none;
  color: #5068a5;
  text-decoration: underline;
  text-decoration-style: dotted;
  margin-bottom: 10px;
  cursor: pointer;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.8s;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
