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

    <b-button href="#" variant="success"><b-icon-cart2></b-icon-cart2> Order</b-button>
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