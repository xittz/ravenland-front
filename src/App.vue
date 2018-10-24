<template>
  <div id="app">
    <div class="bar">
      <div class="container">
        <div class="top-bar-right">
          <a href="https://discord.gg/3448yES"><i class="fab fa-discord"></i></a>
        </div>
      </div>
    </div>
    <Home/>
    <div class="bar footer">
      <div class="top-bar-right">
        <p class="footer-text">RavenLand 2018</p>
      </div>
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'app',
  components: {
    Home
  }
}
</script>

<style>

body {
  margin: 0px;
  font-family: 'Roboto', sans-serif;
}

p {
  font-family: 'Alice', serif;
  font-size: 29px;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.bar {
  height: 45px;
  width: 100%;
  background-color: #f15b22;
}

.top-bar-right {
  height: 100%;
  margin-left: 85%;
}

.fa-discord {
  color: white;
  font-size: 24px;
  padding: 10px;
}

.footer {
  height: 60px;
}

.footer-text {
  color: white;
  font-size: 18px;
  padding: 21px;
  margin: 0px;
}
</style>
