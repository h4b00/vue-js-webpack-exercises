<template>
  <div>
  <slot name="first"></slot>
    <h1>Tez jestem z h1</h1>
  <slot name="second"></slot>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        msg: 'Welcome to Your Vue.js App',
        selectedComponent: ''
      }
    },
    destroyed () {
      console.log('destroy from A')
    },
    activated () {
      console.log('activated from A')
    }
  }
</script>

