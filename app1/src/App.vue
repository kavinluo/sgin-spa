<template>
  <span id="app">
    App1 is working! Yes, this is working; i'm very happy!!
    but this is  no bat
    <p>comment me on and off to see HMR</p>
    <router-view></router-view>
    <br>
    <router-link to="/app2">Go to app2 page home</router-link>

  </span>
</template>

<style>
#app1 {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
