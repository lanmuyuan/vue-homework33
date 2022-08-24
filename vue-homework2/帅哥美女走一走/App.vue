<template>
  <div>
    <ul>
      <li v-for="item in persons " :key="item.id">{{ item.name }}</li>
    </ul>
    <button @click="change">走一走</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      persons: [
        {
          name: '帅哥',
          id: '001',
        },
        {
          name: '美女',
          id: '002',
        },
        {
          name: '程序员',
          id: '003',
        }]
    }
  },
  methods: {
    change(){
      this.persons.push(this.persons.shift());
    }
  }
}
</script>

<style>
</style>
