<template>
  <div id="app">
    <Home />
    <Navigation />
    <Features />
  </div>
</template>

<script>
import Home from '@/components/Home/Home';
import Navigation from '@/components/Navigation/Navigation';
import Features from '@/components/Features/Features';

export default {
  name: 'app',
  components: {
    Home ,
    Navigation,
    Features,
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

:root {
  --main-color: #00A99D;
}

#app {
  font-family: "Raleway", Arial, Helvetica, sans-serif;
}

</style>
