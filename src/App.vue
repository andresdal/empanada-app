<template>
  <div id="app">
    <EmpanadaApp />
  </div>
</template>

<script>
import EmpanadaApp from './components/EmpanadaApp.vue';

export default {
  name: 'App',
  components: {
    EmpanadaApp
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>