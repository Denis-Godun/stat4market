<template>
  <div class="size-item">
    <p class="item pink-item">38</p>
    <p class="item">41</p>
    <p class="item">2 дня</p>
    <p class="item">41шт</p>
    <p class="item">2 дня</p>
    <EditableQuantityButton v-model:value="quantities['item1']" />
    <p class="item">2 дня</p>
    <p class="item">41шт</p>
    <p class="item">2 дня</p>
    <EditableQuantityButton v-model:value="quantities['item2']" />
    <p class="item">5шт/день</p>
    <button>Посмотреть</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

import EditableQuantityButton from "./EditableQuantityButton.vue";

export default defineComponent({
  components: { EditableQuantityButton },
  setup() {
    const quantities = ref({
      item1: "41 шт",
      item2: "244 шт"
    });
    return { quantities };
  },
});
</script>

<style scoped>
.size-item {
  font-family: "Lato Regular";
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  font-size: 14px;
  gap: 15px;
  padding: 0 24px;
  background-color: white;
  border-radius: 4px;
  height: 48px;
  margin: 16px;
}
.item {
  margin-top: auto;
  margin-bottom: auto;
  display: flex;
  align-items: center;
  justify-content: center;
}
.pink-item {
  background: #ea5dbb;
  color: white;
  width: 72px;
  height: 24px;
  border-radius: 4px;
}
button {
  background-color: #5068a5;
  border-radius: 4px;
  width: 84px;
  height: 24px;
  color: white;
  border: none;
  font-size: 12px;
  margin-top: auto;
  margin-bottom: auto;
}
</style>
