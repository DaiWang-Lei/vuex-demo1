<template>
  <div>
    <h1>当前最新的count值为：{{$store.getters.showNum}}</h1>
    <h3>当前最新的count值为：{{$store.state.count}}</h3>
    <button @click="handle1">+1</button>
    <button @click="handle2">+n</button>
    <button @click="handle3">延迟加一 Async</button>
    <button @click="handle4">延迟加N Async</button>


  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    handle1() {
      this.$store.commit('add')
    },
    handle2(){
      this.$store.commit('addN',3)
    },
    handle3(){
      this.$store.dispatch('addAsync')
    },
    handle4(){
      this.$store.dispatch('addNAsync',3)
    }
  }
}
</script>
