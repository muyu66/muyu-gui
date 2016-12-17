<template>
  <div id="app">
    <hello></hello>
  </div>
</template>

<script>
import Hello from './components/Hello'

export default {
  name: 'app',
  components: {
    Hello
  }
}
</script>

<style>
#app {
  color: red;
  height: 100%;
  width: 100%;
  top: 0px;
  left: 0px;
}
</style>
