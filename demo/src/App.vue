<template>
<div id="app">
    <!-- <h1>{{msg}}</h1>
    <img src="./assets/logo.png"> -->
    <router-view />
    <!-- <first/> -->
</div>
</template>

<script>
export default {
    name: 'App',
    data() {
        return {
            msg: "Hello World!"
        }
    }

}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}

#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

h1{
  color: white;
  background-color: rgb(78, 78, 235);
  padding: 1rem
}
</style>
