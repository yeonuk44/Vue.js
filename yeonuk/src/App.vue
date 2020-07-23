<template>
  <div id="app">
    <Header />
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Create from '@/components/Create'
import Detail from '@/components/Detail'
import Read from '@/components/Read'
export default {
  name: 'App',
  components: {
    Header,
    Create,
    Detail,
    Read,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
