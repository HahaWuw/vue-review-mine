<template>
  <div id="app">
    {{a}}, {{b}}, {{c}}
    <!-- 双向数据绑定方法 ：value和$event.target.value -->
    <!-- <input :value="a" @input="a = $event.target.value"> -->
    <hello :num1.sync='a' :num2.sync='b' :num3.sync='c' />
    <!-- <hello :num1.sync='a' :num2.sync='b' :num3.sync='c' @input="num => a= num"/> -->
    <cmp1>
      <!-- 语法糖：#=>v-slot 插槽占位符-->
      <template v-slot:first>
        23333333
      </template>
      <h4>aaa</h4>
      <h4>bbb</h4>
    </cmp1>
    
  </div>
</template>

<script>
import Hello from './components/HelloWorld'
import cmp1 from './components/cmp1'

export default {
  name: 'App',
  data() {
    return {
      a: 1,
      b: 5,
      c: 10
    }
  },
  methods: {
    fn(num) {
      this.a = num
    },
  },
  components: {
    Hello,
    cmp1
  }
}
</script>

<style>

</style>
