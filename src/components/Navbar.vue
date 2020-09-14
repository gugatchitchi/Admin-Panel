<template>
  <div class="navbar">
    <router-link to="/">Home Page</router-link>
    <router-link to="/login">Login Page</router-link>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  components: {}
}
</script>

<style>
  a {
    padding: 0rem 1rem;
    margin: 0rem 1rem;
  }
</style>