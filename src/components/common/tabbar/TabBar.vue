<template>
  <div id="tabbar">
    <slot name="tabbarsllot"></slot>
  </div>
</template>

<script>
export default {
  name:'TabBar',
  components:{}
}
</script>

<style>
#tabbar {
  display: flex;
  background-color: #f6f6f6;
  position:fixed;
  left: 0;
  right: 0;
  bottom: 0;
  box-shadow: 0px -0.09rem 10px rgba(160,160,160,0.3);
  /* z-index: 9; */
}
</style>