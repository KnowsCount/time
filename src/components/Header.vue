<template>
  <div class="header">
    <p class="logo">What Time is it NOT?</p>
    <button v-on:click="alert()">Pay me</button>
  </div>
</template>

<script>
export default {
  // components: {},
  methods: {
    alert() {
      alert(
        "你可以加我微信 `knowscount` 付款，没有二维码主要是因为截图自己的收款太烦了"
      );
    },
  },
};
</script>

<style>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  height: 60px;
  font-family: -apple-system, "Helvetica Neue", sans-serif, Arial, Helvetica;
  background-image: radial-gradient(pink 1px, #fff 1px);
  background-size: 20px 20px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
}

.logo {
  font-weight: 1000;
  font-size: 2em;
  background-color: #fff;
}

button {
  border: none;
  background-color: #fff;
  font-size: 1em;
  font-weight: bold;
  color: #000;
  cursor: pointer;
}
</style>
