<template>
  <div id="app">
    <Navigation></Navigation>
    <router-view></router-view>
    <div class="content">
      <h1 v-if="error" class="text-center">Existió un problema para comunicarse con la API</h1>
      <h1 v-else>Datos Usuarios API:</h1>
      <user v-for="user in users" v-bind:key="user.id" v-bind:user="user" />
    </div>
  </div>
</template>

<style lang="scss">
@import "src/assets/css/styles.scss";
</style>

<script>
// @ is an alias to /src
import axios from "axios";
import User from "./components/User";
import Navigation from "./components/Navigation";

export default {
  name: "App",
  components: {
    User,
    Navigation
  },
  data: function() {
    return {
      users: [],
      error: false
    };
  },
  created() {
    this.callUsers();
  },
  methods: {
    callUsers() {
      axios
        .get("http://127.0.0.1:3000/api/v1/users")
        .then(response => {
          this.users = response.data.data;
        })
        .catch(error => {
          this.error = true;
          console.log("Fallo en comunicación con la API: " + error);
        });
    }
  }
};
</script>
