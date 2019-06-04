<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from '@/components/Header/Header';
export default {
  name: 'app',
  components: {
    Header,
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: "Raleway", Arial, Helvetica, sans-serif;
}
</style>
