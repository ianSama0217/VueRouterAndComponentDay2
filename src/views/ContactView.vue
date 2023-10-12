<script>
import { RouterLink, RouterView } from "vue-router";

export default {
  components: {
    RouterLink,
    RouterView,
  },
  methods: {
    sendContent() {
      alert("成功寄出訊息，請等待回覆。");
    },
  },
};
</script>

<template>
  <form>
    <label for="name">姓名</label>
    <input type="text" name="name" for="name" />
    <label for="email">信箱</label>
    <input type="email" name="email" for="email" />
    <textArea class="content"></textArea>
    <button type="button" @click="sendContent">送出</button>
  </form>
</template>

<style scoped lang="scss">
form {
  height: 25rem;
  width: 30vw;
  display: flex;
  flex-direction: column;
  margin-top: 5rem;
  position: fixed;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);

  label {
    font-size: 1.5rem;
    font-weight: bold;
  }

  input {
    height: 1.5rem;
    border: none;
    margin: 1rem 0;
    background-color: rgba(0, 0, 0, 0.3);
    border-radius: 8px;
  }

  .content {
    height: 10rem;
    border-radius: 8px;
  }

  button {
    margin-top: 1rem;
    height: 2rem;
    width: 8rem;
    align-self: center;
    border: none;
    border-radius: 8px;
    background-color: rgba(0, 0, 0, 0.3);
    font-size: 1.25rem;
    transition: all 0.5s ease;

    &:hover {
      font-weight: bold;
      transform: scale(1.2);
    }
  }
}
</style>
