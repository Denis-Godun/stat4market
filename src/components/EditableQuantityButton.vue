<template>
  <div>
    <button class="quantity" @click="editMode = true" v-if="!editMode">
      {{ newValue }}
    </button>
    <div class="changes" v-else>
      <input v-model="newValue" />
      <button class="action" @click="save">
        <img src="../img/icons/action_btns.svg" alt="" />
      </button>
      <button class="action" @click="cancel">
        <img src="../img/icons/cross.svg" alt="" />
      </button>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref, watch, defineProps, defineEmits } from "vue";

// Определяем пропсы
const props = defineProps<{ value: string }>();

// Определяем событие для поднятия изменений
const emit = defineEmits<{ (e: "update:value", value: string): void }>();

// Локальная переменная для редактирования
const newValue = ref(props.value);
const editMode = ref(false);

// Следим за изменением пропса value
watch(
  () => props.value,
  (newVal) => {
    newValue.value = newVal;
  }
);

const save = () => {
  // Поднимаем событие для обновления value в родительской компоненте
  emit("update:value", newValue.value);
  editMode.value = false;
};

const cancel = () => {
  newValue.value = props.value;
  editMode.value = false;
};
</script>

<style scoped>
.quantity {
  background-color: white;
  border: none;
  color: #5068a5;
  text-decoration: underline;
  text-decoration-style: dotted;
  margin-bottom: 10px;
  cursor: pointer;
  font-size: 14px;
}
.action {
  background-color: white;
  border: none;
  cursor: pointer;
  width: 20px;
  height: 20px;
}
input {
  border: none;
}
.changes {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
