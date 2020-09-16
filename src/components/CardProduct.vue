<template>
  <b-card
    :title="product.nama"
    :img-src="'assets/images/'+product.gambar"
    img-alt="Image"
    img-top
    tag="article"
    class="mb-2 shadow card-product"
  >
    <b-card-text>
      Harga : Rp. {{product.harga}}
    </b-card-text>

    <router-link :to="'/foods/'+product.id" class="btn btn-success"><b-icon-cart2></b-icon-cart2> Order</router-link>
  </b-card>
</template>

<script>
export default {
  name: "CardProduct",
  props: ['product']
};
</script>

<style>
</style>