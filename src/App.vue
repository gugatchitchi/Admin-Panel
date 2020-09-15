<template>
  <!-- <Navbar /> -->
  <router-view/>
</template>

<script>
// import Navbar from '@/components/Navbar.vue'
export default {
  name: '#app',
  components: {
    // Navbar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

#app {
  font-family: 'Source Sans Pro', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
* {
  font-family: 'Source Sans Pro', sans-serif;
  margin: 0;
  padding: 0;
}

</style>
