<template>
  <svg class="icon" aria-hidden="true">
    <use :xlink:href="`#icon-${name}`"></use>
  </svg>
</template>


<script>
import './svg'

export default {
  name:'icon',
  props:['name'],
}
</script>


<style scoped>
  .icon {
  width: 1em;
  height: 1em;
  /* vertical-align: -0.15em; */
  fill: black;
  overflow: hidden;
  }
</style>
