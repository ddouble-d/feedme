<template>
  <div>
    <Navbar />
    <div class="container">
      <div class="row mt-4">
        <div class="col">
          <h2>
            Daftar
            <strong>Makanan</strong>
          </h2>
        </div>
      </div>
      <div class="row mt-3">
        <div class="col">
          <b-input-group size="lg">
            <template v-slot:append>
              <b-input-group-text>
                <b-icon-search></b-icon-search>
              </b-input-group-text>
            </template>
            <b-form-input v-model="search" @keyup="onSearch" placeholder="Search your favorite menu..."></b-form-input>
          </b-input-group>
        </div>
      </div>
      <div class="row mb-4">
        <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
          <CardProduct :product="product" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "Foods",
  components: {
    Navbar,
    CardProduct,
  },
  data() {
    return {
      products: [],
      search: ''
    };
  },
  methods: {
    getProduct(data) {
      this.products = data;
    },
    onSearch() {
      axios
      .get("http://localhost:3000/products?q="+this.search)
      .then((response) => {
        this.getProduct(response.data);
      })
      .catch((error) => {
        console.log(error);
      });
    }
  },
  mounted() {
    axios
      .get("http://localhost:3000/products")
      .then((response) => {
        this.getProduct(response.data);
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>


<style>
</style>