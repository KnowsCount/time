<template>
  <Header />
  <Clock />
</template>

<script>
import Clock from "./components/Clock.vue";
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Clock,
    Header,
  },
};
</script>
