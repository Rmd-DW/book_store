<template>
    <div class="card bg-secondary" style="width: 18rem;">
      <img :src="getImageUrl(product.imagen)" class="card-img-top" :alt="product.nombre" width="100%" height="300px">
      <div class="card-body">
        <h3 class="card-title">{{ product.nombre }}</h3>
        <p class="card-text text-light">{{ product.descripcion }}</p>
        <p class="card-text text-light">Precio: ${{ product.precio }}</p>
        <p class="card-text text-light">Stock Disponible: {{ product.stock }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductCard',
    props: {
      product: {
        type: Object,
        required: true
      }
    },
    methods: {
      getImageUrl(imagePath) {
     
        return `/imgs/${imagePath}`;
      }
    }
  };
  </script>
  
  <style scoped>

  </style>
  