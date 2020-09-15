<template>
  <div class="colorful-block" :style="{ backgroundColor: color }">
    <h1>{{ name }}</h1>
    <!-- <hr/> -->
    <h3>{{ numberWithCommas(value) }}</h3>
  </div>
</template>

<script>
export default {
  name: 'ColorfulBlock',
  props: [
    'color',
    'name',
    'value'
  ],
  methods: {
    numberWithCommas(x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",") + ' ₾.';
    },
  },
}
</script>

<style scoped>
.colorful-block {
 color: white;
 padding: 1em;
 margin: 2em;
 position: relative;
 border-radius: 10px;
}
h1 {
  font-size: 1.4em;
  font-weight: 600;
  padding: 0.5em;
}
h3 {
  padding: 0.5em;
  font-weight: 500;
}
</style>