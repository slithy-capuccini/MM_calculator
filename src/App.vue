<template>
  <HelloWorld msg="Calculadora Masa molar"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld  
  },
}
</script>

<style>
.center {
  text-align: center;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  margin-top: 0px;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>
