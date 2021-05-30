<template>
  <div id="profile">
    我的
    <!-- <ebutton>
      <template v-slot:one='slotone'>
        {{slotone.value1}}
      </template>
    </ebutton> -->
  </div>
</template>

<script>
import ebutton from 'components/slottest/Test.vue'
export default {
  name:'Profile',
  components:{
    ebutton
  },
 created(){
    console.log('profile被创建')
  },
  destroyed(){
    console.log('profile被销毁')
  }
}
</script>

<style>

</style>