<template>
  <div id="app">
    <v-app>
      <div id="nav">
        <span class="group-nav">
          <router-link to="/">Pronóstico del día</router-link>
          <router-link to="/forecast">Pronóstico para la semana</router-link>
          <router-link to="/history">Pronósticos anteriores</router-link>
        </span>
        <Selectors/>
      </div>
      <router-view/>
    </v-app>
  </div>
</template>

<script>
// @ is an alias to /src

import Selectors from "@/components/Selectors.vue";

export default {
  name: "app",
  components: {
    Selectors
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  background-color: #eb5d09;
  text-align: left;
  box-shadow: 0px 1px 3px 0px #bcb9b9;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

#nav a:hover {
  background-color: #e15809;
}

#nav a {
  color: white;
  text-decoration: none;
  font-size: 15px;
  padding: 15px;
}

#nav a.router-link-exact-active {
  background-color: #e15809;
  font-weight: bold;
}

.group-nav {
  display: flex;
}
</style>
