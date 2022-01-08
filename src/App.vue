<template>
  <div class="container">
    <Navbar />
    <router-view />
  </div>
  <Footer />
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style>
.container {
  background-size: cover;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>
