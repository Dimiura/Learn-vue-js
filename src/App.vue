<template>
  <TheHeader v-if="showHeader" />
  <div v-show="showName">
    Nome: {{ name }}
    <br>
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="accessLevel=='admin'">Admin</div>
  <div v-else-if="accessLevel == 'patient'">Paciente</div>
  <div v-else>User</div>

  
</template>

<script>

import TheHeader from './components/TheHeader'; 

export default {
  name: 'App',
  components: {
    TheHeader
  },
  data() {
      return {
      showHeader:true,
      name:"Diego",
      lastName: "Miura",
      showName:false,
      accessLevel: ""
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
  margin-top: 60px;
}
</style>
