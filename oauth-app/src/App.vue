<template>
  <div id="app" class="main-container">
    <b-navbar toggleable="lg" type="dark" variant="dark" class="navbar">
      <b-navbar-brand>
        <b-link :to="{ name: 'home' }" class="brand-link">Inicio</b-link>
      </b-navbar-brand>
      <b-navbar-toggle target="nav-bar"></b-navbar-toggle>
      <b-collapse id="nav-bar" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item v-if="$auth.isAuthenticated">
            <b-link :to="{ name: 'profile' }" class="nav-link">Perfil</b-link>
          </b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <b-container class="content-container">
      <router-view/>
    </b-container>
  </div>
</template>

<script>
export default {
};
</script>

<style scoped>
.main-container {
  padding: 20px;
  background-color: #f0f2f5;
}

.navbar {
  background-color: #343a40;
  border-radius: 8px;
  padding: 10px 20px;
}

.brand-link {
  color: #ffffff;
  font-weight: bold;
  font-size: 1.2rem;
}

.nav-link {
  color: #f0f2f5;
  font-weight: 500;
  padding: 0 10px;
}

.content-container {
  margin-top: 20px;
  background-color: #ffffff;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
</style>
