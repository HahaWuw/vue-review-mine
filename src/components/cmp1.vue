<template>
  <div>
    <h4>ccc</h4>
    <slot name="first"></slot>
    <slot />
    <h4>ddd</h4>
    <!-- <button @click="$emit('update:num1', num1+5);$emit('update:num2', num2+10);$emit('update:num3', num3+15);">增加</button> -->
  </div>
</template>

<script>
export default {
  props:['num1', 'num2', 'num3'],
  name: 'HelloWorld',
  data () {
    return {
      msg: '111'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
