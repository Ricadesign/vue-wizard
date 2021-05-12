<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <rica-vue-stepper :steps="routes"></rica-vue-stepper>
    <router-view/>
  </div>
</template>

<script>
import RicaVueStepper from './components/RicaVueStepper.vue'
import { routes } from "./router/index";
export default {
  components: { RicaVueStepper },
  data: () => ({
    routes: routes,
  }),
  setup() {
    
  },
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
