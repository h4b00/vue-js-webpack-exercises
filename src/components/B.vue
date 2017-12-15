<template>
  <div>
    <h1></h1>
    <button @click="counter++">Counter++</button>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        counter: 0
      }
    },
    destroyed () {
      console.log('destroy from B')
    },
    activated () {
      console.log('activated from ')
    }
  }
</script>

