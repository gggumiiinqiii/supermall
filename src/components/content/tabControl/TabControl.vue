<template>
  <div class="tab-control">
    <div class="tab-control-item" 
    @click="change(index)"
    v-for="(item,index) in title" :key="index"
    :class="{active:index === currentindex}">
      <span>{{title[index]}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name:'TabControl',
  props:{
    title:{
      type:Array,
      default(){
        return[]
      }
    }
  },
  methods:{
    change(index){
      this.currentindex = index
    }
  },
  data(){
    return {
      currentindex:0
    }
  }
}
</script>

<style >
.tab-control {
  display: flex;
  height: 40px;
  line-height: 40px;
  text-align: center;
  font-size: 15px;
  background-color: #fff;
}
.tab-control-item {
  flex: 1;
}
.tab-control-item span {
  padding: 5px;
}
.active {
  color: var(--color-high-text);
  
}
.active span {
  border-bottom: 3px solid var(--color-tint);
}
</style>