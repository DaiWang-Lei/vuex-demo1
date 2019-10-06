<template>
  <div>
    <h3>当前最新的count值为：{{count}}</h3>
    <h4>当前最新的count值为：{{showNum}}</h4>
    <button @click="sub">-1</button>
    <button @click="subN(3)">-N</button>
    <button @click="subAsync">-1 Async</button>
    <button @click="subNAsync(3)">-N Async</button>


  </div>
</template>

<script>
import { mapState,mapActions ,mapMutations,mapGetters} from 'vuex'
export default {
  data() {
    return {}
  },
  methods: {
    ...mapActions(['subAsync','subNAsync']),
    ...mapMutations(['sub','subN']),
  },
  computed: {
    ...mapGetters(['showNum']),
    ...mapState(['count'])
  }
}
</script>
