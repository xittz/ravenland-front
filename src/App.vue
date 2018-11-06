<template>
  <div id="app">
    <nav class="navbar">
      <div class="navbar-end">
        <a class="navbar-item" v-scroll-to="{element: '#team', duration: 1000}">
          Team
        </a>
        <a class="navbar-item" href="https://discord.gg/3448yES"><i class="fab fa-discord fa-hover"></i></a>
      </div>
    </nav>
    <Home/>
    <div class="bar foot">
      <div class="down-bar-right">
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

html {
    position: relative;
    min-height: 100%;
}

body {
  margin: 0px;
  margin-bottom: 60px;
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

.navbar {
  background-color: #f15b22;
}

.navbar-item {
  color: white;
}

.navbar-item:hover {
  color: #2e3e80;
}

.navbar-item:hover .fa-discord {
  color: #2e3e80;
}

.fa-hover:hover {
  color: #2e3e80;
}



.top-bar-right {
  height: 100%;
  margin-left: 85%;
}

.down-bar-right {
  height: 100%;
  margin-left: 80%;
}

.nav-link {
  color: white;
  font-size: 18px;
  padding: 12px;
}

.nav-link:hover{
  cursor: pointer;
}

.fa-discord {
  color: white;
  font-size: 24px;
}

.foot {
  height: 60px;
  position: absolute;
  left: 0;
  bottom: 0;
  overflow:hidden;
}

.footer-text {
  color: white;
  font-size: 18px;
  padding: 21px;
  margin: 0px;
}
</style>
