<template>
  <div class="panel-header">
    <h1>{{ name }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Panel Header',
  props: [
    'name'
  ]
}
</script>

<style scoped>
h1 {
  padding: 1em 0;
  color: #636261;
}

/* For Larger Screens */
@media (min-width: 800px) {
  h1 {
    text-align: left;
    padding: 1em;
  }
}
</style>