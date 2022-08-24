<template>
  <div>
    <ul>
      <li v-for="(item,index) in random" :key="index">{{item}}<button @click="del(index)">删除</button></li>
    </ul>
    <button @click="add">添加</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      random:[]
    }
  },
  methods:{
    add(){
      this.random.push(Math.floor(Math.random()*20))
    },
    del(index){
      this.random.splice(index,1)
    }
  }
}
</script>

<style>

</style>
