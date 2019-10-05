<template>
  <div>
    <my-addition></my-addition>

    <div>-------------------------</div>

    <my-subtraction></my-subtraction>
  </div>
</template>

<script>
import Addition from './components/Addition'
import Subtraction from './components/Subtraction'
export default {
  data() {
    return {}
  },
  components: {
    'my-addition': Addition,
    'my-subtraction': Subtraction
  }
}
</script>
