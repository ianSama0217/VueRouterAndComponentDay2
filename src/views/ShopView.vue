<script>
import { RouterLink, RouterView } from "vue-router";
import card from "../components/card.vue";

export default {
  components: {
    RouterLink,
    RouterView,
    card,
  },
};
</script>

<template>
  <h1>歡迎來到線上商城</h1>
  <div class="productArea">
    <card productName="西瓜" productValue="50" />
    <card productName="香蕉" productValue="25" />
    <card productName="蘋果" productValue="30" />
    <card productName="葡萄" productValue="100" />
  </div>
</template>

<style scoped lang="scss">
h1 {
  color: block;
}

.productArea {
  display: flex;
  flex-wrap: wrap flex;
  justify-content: space-around;
  margin-top: 5vh;
}
</style>
