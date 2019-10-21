<template>
  <b-navbar type="dark">
    <b-navbar-brand href="#" exact>
      <img src="favicon.ico" class="d-inline-block align-top" alt="Kitten" />
    </b-navbar-brand>
    <b-navbar-nav>
      <b-nav-item href="#">Usuarios</b-nav-item>
      <b-nav-item-dropdown text="Test" left>
        <b-dropdown-item href="#">Item1</b-dropdown-item>
        <b-dropdown-item href="#">Item2</b-dropdown-item>
        <b-dropdown-item href="#">Item3</b-dropdown-item>
      </b-nav-item-dropdown>
    </b-navbar-nav>
    <b-navbar-nav class="ml-auto">
      <router-link to="/login">Login</router-link>
    </b-navbar-nav>
  </b-navbar>
</template>

<script>

export default {
  name: "Navigation", //this is the name of the component
};
</script>