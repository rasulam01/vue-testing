

<script>
import HelloWorld from './components/HelloWorld.vue'
import ShitPants from './components/testingthings.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ShitPants
  }
}

</script>


<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="une belle vue" /> 
  
  <div>
    <ShitPants v-bind:shit="5**5" />
    <button>Plus</button>
  </div>
</template>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 90px;
}
</style>
