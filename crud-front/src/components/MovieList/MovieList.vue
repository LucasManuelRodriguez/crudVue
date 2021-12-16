<template>
  <div>
    <h1> Lista de Pelis</h1>
    <ul>
      <li v-for="(movie,index) in movies" :key="index">
        {{index}} - {{movie.title}}
      </li>
    </ul>
    <input type="text" v-model="newMovie.title" />
    <button @click="addMovie">Add</button>
    <p>{{newMovie.title}}</p>

  </div>
</template>

<script>
export default {
  data(){
    return{
      newMovie:{},
      movies:[
        {
        title:'Terminator 2',
        },
        {
        title:'Rapido y Furioso',
        },
        {
        title:'La Máscara',
        }
        ],
    }
  },
  methods:{
    addMovie(){
      if(!this.newMovie.title) return;
      this.movies = [...this.movies, this.newMovie];
      this.newMovie ={};
    }
  }

};
</script>

<style>
ul{
  list-style: none;
}
</style>