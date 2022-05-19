<template>
<div class="container mb-5">
    <h1 class="text-center mb-5">Peliculas en cartelera</h1>
    <div class="row justify-content-center">
      <div
        class="card text-white bg-dark  col-12 col-sm-3 m-4 shadow-lg p-3 mb-5  rounded "
        v-for="(item, index) in result"
        :key="index"
      >
        <img
          class="card-img-top"
          v-bind:src="item.poster_path"
          v-bind:alt="item.title"
        />
 
        <div class="card-body">
          <h5 class="card-title">{{ item.title }}</h5>
          <p class="card-text">Titulo Original: {{ item.original_title }}</p>
          <p class="card-text">Descripcion: {{ item.overview }}</p>
        </div>
      </div>
    </div>
  </div>

  
</template>

<script>
export default {

}
</script>

<style>

</style>