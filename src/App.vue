<template>
  <div id="app">
    <Home />
    <Navigation />
  </div>
</template>

<script>
import Home from '@/components/Home/Home';
import Navigation from '@/components/Navigation/Navigation';

export default {
  name: 'app',
  components: {
    Home ,
    Navigation,
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: "Raleway", Arial, Helvetica, sans-serif;
}
</style>
