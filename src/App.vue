<script>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div class="navBar">
    <RouterLink to="/" class="link">首頁</RouterLink>
    <RouterLink to="about" class="link">關於</RouterLink>
    <RouterLink to="contact" class="link">聯絡我們</RouterLink>
    <RouterLink to="shop" class="link">商城</RouterLink>
  </div>
  <RouterView></RouterView>
</template>

<style scoped lang="scss">
.navBar {
  background-color: #777;
  height: 10vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: sticky;
  top: 0%;

  .link {
    font-size: 1.5rem;
    text-decoration: none;
    color: aliceblue;
    transition: all 0.5s ease;

    &:hover {
      cursor: pointer;
      color: black;
      font-weight: bold;
    }
  }
}
</style>
