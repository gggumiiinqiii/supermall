<template>
  <div class="button">
    <button></button>
    <!-- 首先在子组件得slot上动态绑定一个值(:key='vlue')
         然后在父组通过v-slot:name="values"将这个值付给values
         最后通过{{vlues.key}}得方式获取数据
     -->
    <slot name="one" :value1="child1"></slot>
  </div>
</template>

<script>
export default {
  data(){
    return {
      child1:'数据133'
    }
  }
}
</script>

<style>

</style>