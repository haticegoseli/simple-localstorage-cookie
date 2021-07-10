<template>
  <div id="app" class="container">
    <div class="row">
      <h2>Local Storage and Cookie</h2>
      <hr>
      <br>
    </div>
    <div class="row">
      <div class="col-md-6">
        <LocalStorage/>
      </div>
      <div class="col-md-6">
        <Cookie/>
      </div>
    </div>
  </div>
</template>

<script>
import LocalStorage from './components/LocalStorage.vue'
import Cookie from "./components/Cookie"

export default {
  name: 'App',
  components: {
    LocalStorage,
    Cookie
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h2 {
  font-weight: bold;
}
label {
  float: left;
  font-weight: bold;
}
p{
  text-align: left;
}

</style>
