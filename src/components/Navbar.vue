<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="transparent">
      <div class="container">
        <b-navbar-brand href="#">FeedMe</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item>
              <router-link class="nav-link" to="/">Home</router-link>
            </b-nav-item>
            <b-nav-item>
              <router-link class="nav-link" to="/foods">Foods</router-link>
            </b-nav-item>
          </b-navbar-nav>

          <b-navbar-nav class="ml-auto">
            <b-nav-item>
              <router-link class="nav-link" to="/cart">
                Cart
                <b-icon-handbag></b-icon-handbag>
                <span class="badge badge-success ml-2">0</span>
              </router-link>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>