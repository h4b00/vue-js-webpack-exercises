<template>
  <div>
    <keep-alive>
      <component :is="selectedComponent"></component>
    </keep-alive>
    <button @click="selectedComponent='Acomp'">Show me Acomp</button>
    <button @click="selectedComponent='Bcomp'">Show me Bcomp</button>
    <acomp>
      <h1 slot="first">{{sampleText}}</h1>
      <h2 slot="second">Second text</h2>
    </acomp>
    <bcomp>Bye World</bcomp>
  </div>
</template>

<script>
  import A from '@/components/A'
  import B from '@/components/B'
export default {
    name: 'HelloWorld',
    data: () => {
      return {
        selectedComponent: '',
        sampleText: 'Test'
      }
    },
    components: {
      'Acomp': A,
      'Bcomp': B
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  color: red;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
