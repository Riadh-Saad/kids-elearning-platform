<template>
  <header class="container">
    <Navbar />
    <div>
      <Header :func="notify" />
    </div>
  </header>
</template>

<script>
import Header from "./components/Header.vue";
import Navbar from './components/Navbar.vue';
import Animals from './components/Animals.vue'


export default {
  components: { Header, Navbar,Animals },
  name: "App",  methods: {
    playSound (sound) {
      if(sound) {
        var audio = new Audio(sound);
        audio.play();
      }
      }, notify() {
      alert('navigation was prevented.')
    }
      }
};
</script>

<style>


</style>
