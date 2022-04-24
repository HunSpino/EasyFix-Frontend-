<template>
  <div id="app">
    <header>
      <img alt="EF logo" src="./assets/ef_logo.png">
      <h1>Üdvözöllek az EasyFix vendégoldalán</h1>
      <ul class="nav">
        <li class="nav-item">
          <a class="nav-link" href="http://127.0.0.1:8000/login">Bejelentkezés</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="http://127.0.0.1:8000/register">Regisztráció</a>
        </li>
      </ul>
    </header>
    <GepekList/>
  </div>
</template>

<script>
import GepekList from './components/GepekList.vue'

export default {
  name: 'App',
  components: {
    GepekList
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
</style>
