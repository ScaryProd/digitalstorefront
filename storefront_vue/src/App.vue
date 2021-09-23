<template>
  <div id="wrapper">
    <nav class="navbar is-dark">
      <div class="navbar-brand">
        <router-link to="/" class="navbar-item">
          <strong>Storefront</strong></router-link
        >

        <a
          class="navbar-burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navbar-menu"
          @click="showMobileMenu = !showMobileMenu"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div
        class="navbar-menu"
        id="navbar-menu"
        v-bind:class="{ 'is-active': showMobileMenu }"
      >
        <div class="navbar-end">
          <router-link to="/vending" class="navbar-item"
            >Vending Machines</router-link
          >
          <router-link to="/nuts" class="navbar-item">Nuts</router-link>

          <div class="navbar-item">
            <div class="buttons">
              <router-link to="/log-in" class="button is-light"
                >Log in</router-link
              >

              <router-link to="/cart" class="button is-success">
                <span class="icon"><em class="fas fa-shopping-cart"></em></span>
                <span>Carrito</span>
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </nav>

    <section class="hero is-medium is-dark mb-6">
      <div class="hero-body has-text-centered">
        <p class="title mb-6">Welcome to the Digital Storefront</p>
        <p class="subtitle">The #1 place to stock your machines</p>
      </div>
    </section>

    <footer class="footer">
      <p class="has-text-centered">Copyright (c) 2021</p>
    </footer>
  </div>
</template>

<script>
export default {
  setup() {
    return {
      showMobileMenu: false,
    };
  },
};
</script>

<style lang="scss">
@import "../node_modules/bulma";
</style>
