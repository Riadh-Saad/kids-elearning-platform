<template>
  <header class="container">
    <Navbar/>
    <div>
      <Header />
    </div>
  </header>
</template>

<script>
import Header from "./components/Header.vue";
import Navbar from './components/Navbar.vue';

export default {
  components: { Header, Navbar },
  name: "App",
};
</script>

<style>


</style>
