<template>
    <div class="card" style="width: 18rem; height: 40rem;">
      <img :src="getImageUrl(product.imagen)" class="card-img-top" :alt="product.nombre" width="100%" height="300px">
      <div class="card-body">
        <h3 class="card-title">{{ product.nombre }}</h3>
        <p class="card-text">{{ product.descripcion }}</p>
        <p class="card-text">Precio: ${{ product.precio }}</p>
        <p class="card-text">Stock Disponible: {{ product.stock }}</p>
        <AddToCartButton @add-to-cart="addToCart" :product="product" />
      </div>
      
    </div>
  </template>
  
  <script>
  import AddToCartButton from './AddToCartButton.vue'
  
  export default {
    name: 'BookCard',
    props: {
      product: {
        type: Object,
        required: true
      }
    },
    components: {
      AddToCartButton
    },
    methods: {
      addToCart() {
        this.$emit('add-to-cart', this.product)
      },
      getImageUrl(imagePath) {
        return `${process.env.BASE_URL}${imagePath}`;
      }
    }
  }
  </script>
  
  <style scoped>
  .card {
   
    box-shadow: 0 0 5px #454545;
    margin: 1rem;
    text-align: center;
    border-radius: 10px;
  }
  </style>
  