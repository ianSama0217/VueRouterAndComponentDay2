<script>
export default {
  name: "card",
  props: {
    productName: { type: String, required: true, default: null },
    productValue: { type: Number, required: true, default: 0 },
  },
  data() {
    return {
      count: 1,
    };
  },
  //   components: {
  //     RouterLink,
  //   },
  methods: {
    buy() {
      let sumValue = 0;
      sumValue = this.productValue * this.count;

      alert("購買成功!一共是$ " + sumValue + "元!");
    },
  },
};
</script>

<template>
  <div class="cardBox">
    <h3>商品名稱: {{ productName }}</h3>
    <h5>商品價格:$ {{ productValue }}</h5>
    <label for="count">購買數量</label>
    <input type="number" name="count" for="count" min="1" v-model="count" />
    <button type="button" @click="buy">購買</button>
  </div>
</template>

<style scoped lang="scss">
.cardBox {
  width: 20vw;
  height: 50vh;
  border: 3px solid #777;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: start;
  padding: 1rem;

  h3 {
    font-size: 1.5rem;
  }

  h5 {
    font-size: 1.5rem;
  }

  label {
    font-size: 1.25rem;
    font-weight: bold;
  }

  input {
    height: 1.5rem;
    width: 12rem;
  }

  button {
    align-self: center;
    height: 2rem;
    width: 6rem;
    border-radius: 8px;
    border: 1px solid #777;
    font-size: 1.15rem;
    transition: all 0.5s ease;

    &:hover {
      background-color: #232323;
      color: white;
      font-weight: bold;
    }
  }
}
</style>
