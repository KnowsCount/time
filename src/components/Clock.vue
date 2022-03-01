<template>
  <div class="clock">
    <div class="date">
      {{ date }}
    </div>
    <div class="time">
      <span>{{ hour }}<span class="blink">:</span>{{ min }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hour: this.genRandomInt(0, 24),
      min: this.genRandomInt(0, 60),
      date: this.getDate(),
    };
  },
  methods: {
    genRandomInt(min, max) {
      min = Math.ceil(min);
      max = Math.floor(max);
      let randomInt = Math.floor(Math.random() * (max - min + 1)) + min;
      return randomInt;
    },
    getDate() {
      return new Date().toJSON().slice(0, 10);
    },
  },
  mounted() {
    if (this.hour < 10) {
      this.hour = `0${this.hour}`;
    }
    if (this.min < 10) {
      this.min = `0${this.min}`;
    }
    // console.log(`${this.hour}:${this.min}`);
  },
};
</script>

<style lang="scss">
html,
body {
  height: 100%;
  background-color: #e5e5f7;
  // opacity: 0.2;
  background-image: radial-gradient(#444cf7 1px, #e5e5f7 1px);
  background-size: 20px 20px;
}
span {
  margin: 0;
  padding: 0;
}
.blink {
  animation: blink 2s infinite steps(1);
}
@keyframes blink {
  50% {
    color: transparent;
    text-shadow: none;
  }
}
.clock {
  // z-index: 999;
  font-family: monospace;
  color: black;
  text-align: center;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  color: black;
  // text-shadow: 0 0 20px rgba(10, 175, 230, 1), 0 0 20px rgba(10, 175, 230, 0);
  .time {
    letter-spacing: 0.05em;
    font-size: 80px;
    padding: 5px 0;
  }
  .date {
    letter-spacing: 0.1em;
    font-size: 24px;
  }
  .text {
    letter-spacing: 0.1em;
    font-size: 12px;
    padding: 20px 0 0;
  }
}
</style>
