<template>
  <div class="sidebar">
    <div class="logo">
      <img src="../img/icons/logo.svg" alt="" />
    </div>
    <div class="menu">
      <div class="menu-item">
        <img src="../img/icons/navbar_icon.svg" alt="" class="nav_icons" />
        <div>Мой склад</div>
      </div>
    </div>
    <div class="bottom">
      <div class="bottom-contacts">
        <a href="#"><img src="../img/icons/instagramm.svg" alt="" /></a>
        <a href="#"><img src="../img/icons/telegramm.svg" alt="" /></a>
        <a href="#"><img src="../img/icons/vk.svg" alt="" /></a>
      </div>

      <p><a href="#">Партнерская программа</a></p>
    </div>
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
.sidebar {
  width: 240px;
  min-height: 100vh;
  background-color: #182246;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.logo {
  display: flex;
  align-items: center;
  height: 80px;
}
.logo img {
  padding-left: 24px;
}

.menu {
  height: 100%;
  padding-top: 12px;
}
.menu-item {
  padding-left: 24px;
  display: flex;
  align-items: center;
}
.menu-item div {
  color: white;
  font-family: "Lato Semibold";
  font-size: 14px;
  padding-left: 16px;
  vertical-align: middle;
}
.bottom {
  height: 90px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 16px;
}
.bottom-contacts {
  display: flex;
  justify-content: center;
  gap: 24px;
}
.bottom p {
  margin-bottom: 24px;
}
.bottom p a {
  color: #717b9e;
  text-decoration-style: dotted;
  text-underline-offset: 5px;
  font-family: "Lato Regular";
}
</style>
