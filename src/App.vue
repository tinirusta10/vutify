<template>
<v-app>
  <v-toolbar class="red">
    <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    <v-toolbar-title style="color: white;" class="text-uppercase">River</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn  class="red">Instagram</v-btn>
      <v-btn  class="red">Facebook</v-btn>
      <v-btn  class="red">Twitter</v-btn>
    </v-toolbar-items>
  </v-toolbar>
  
  <v-navigation-drawer v-model="drawer" style="width: 300px;" temporary app class="white">
    <v-list>
      <v-list-subheader class="black--text">River</v-list-subheader>
      <v-list-item v-for="item in links" :key="item.texto" router :to="item.ruta">
          <v-icon class="gray--text" >{{ item.icono }}</v-icon>
        <v-list-item-title class="gray--text" v-text="item.texto"></v-list-item-title>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
  <v-content>
    <router-view/>
  </v-content> 
</v-app>
</template>

<script>
export default{
data() {
  return {
    drawer:false,
    links:[
      {icono:'mdi-checkbox-marked-circle',texto:'Proximos partidos',ruta:'/proximos'},
      {icono:'mdi-checkbox-marked-circle',texto:'Links',ruta:'/links'},
      {icono:'mdi-checkbox-marked-circle',texto:'Twitter',ruta:'a'}
    ]
  }
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
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
