<template>
  <div>
    <h1> Lista de Pelis</h1>
    <ul>
      <li v-for="(movie,index) in movies" :key="index">
        titulo
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      movies:[1,2,3],
    }
  }

};
</script>

<style>
ul{
  list-style: none;
}
</style>