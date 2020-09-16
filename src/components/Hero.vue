<template>
  <div class="hero">
    <!-- Desktop view -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu,</strong>
                <br />in Your Gadget
              </h2>
              <p>Choose & order your favorite menu!</p>
              <router-link to='/foods' class="btn btn-lg btn-success">
                <b-icon-arrow-right></b-icon-arrow-right> Order
              </router-link>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/hero.svg" width="100%" alt />
        </div>
      </div>
    </div>

    <!-- Mobile view -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
          <div class="col-md-6 mb-4">
          <img src="../assets/images/hero.svg" width="100%" alt />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu,</strong>
                <br />in Your Gadget
              </h2>
              <p>Choose & order your favorite menu!</p>
              <button class="btn btn-lg btn-success">
                <b-icon-arrow-right></b-icon-arrow-right> Order
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style>
</style>