<script setup lang="ts">

  interface Guitarra {
    id: number,
    nombre: string,
    descripcion: string,
    imagen: string,
    precio: number
  }

  const props = defineProps<{
    guitarra: Guitarra;
  }>();

  const {id, nombre, descripcion, imagen, precio} = props.guitarra

</script>
<template>
  <div key="id" class="col-md-6 col-lg-4 my-4 row align-items-center">
    <div class="col-4">
      <img class="img-fluid" :src="`/img/${imagen}.jpg`" alt="imagen guitarra">
    </div>
    <div class="col-8">
      <h3 class="text-black fs-4 fw-bold text-uppercase">{{ nombre }}</h3>
      <p>{{ descripcion }}</p>
      <p class="fw-black text-primary fs-3">{{ precio }}</p>
      <button
          type="button"
          class="btn btn-dark w-100 "
      >Agregar al Carrito</button>
    </div>
  </div>
</template>
