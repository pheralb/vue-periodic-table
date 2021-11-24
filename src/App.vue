<template>
  <div id="app">
    <Table />
  </div>
</template>

<script>
import Table from './components/Table.vue'

export default {
  name: 'App',
  components: {
    Table
  }
}
</script>

<style>
@font-face {
  font-family: Poppins-Regular;
  src: url(assets/fonts/Poppins-Regular.ttf);
}

body {
  font-family: Poppins-Regular;
}
</style>
