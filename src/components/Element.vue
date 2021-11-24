<template>
  <div class="element" :style="attr">
    <h1>{{ atomicNumber }}</h1>
    <span>{{ name }}</span>
  </div>
</template>

<!-- elementData.cpkHexColor -->

<script>
export default {
  name: 'Element',
  props: {
    name: { type: String },
    atomicNumber: { type: Number },
    color: { type: String }
  },
  data() {
    return {
      attr: {
        "--color": `#${this.color}`
      }
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.element {
  background-color: var(--color);
  border: 1px solid rgb(182, 182, 182);
  border-radius: 10px;
  padding: 10px;
  text-align: center;
  margin: 5px;
  transition: transform 0.2s;
}
.element:hover {
  transform: scale(1.07);
  border: 1px solid rgb(231, 186, 63);
}
</style>
