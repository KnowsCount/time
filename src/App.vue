<template>
  <Header />
  <Clock />
  <Footer />
</template>

<script>
import Clock from "./components/Clock.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Clock,
    Header,
    Footer,
  },
};
</script>
