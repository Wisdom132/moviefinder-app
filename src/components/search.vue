<template> 
    <div>

      <div class="container">
        <div class="row mt-5 mb-5">
          <div class="offset-md-6 col-md-6">
              <form class="d-flex">
              <input type="text" placeholder="Enter a movie title" class="col-md-6 mr-3 search form-control" v-model="search" ref="input" >
              <button @click.prevent="submit" class="btn">search</button>
            </form> 
          </div>
        </div>
        <div class="row mt-5 mb-5">
          <div class="col-md-6">
            <img :src= movie.Poster alt="" class="img-fluid">
          </div>
          <div class="col-md-6">
            <h3 class="movieName">{{ movie.Title}}</h3>
            <h6 class="movieSub"><span>{{movie.Rated}}</span> <span>{{movie.Year}}</span> <span>{{movie.Genre}}</span> <span>{{movie.Released}}</span></h6>
            <h3 class='moviePlot mt-3 mb-3'>{{movie.Plot}}</h3>
            <h3 class="MovieWriter mt-2 mb-3">Written by:<span class="writer">{{movie.Writer}}</span></h3>
            <h3 class="MovieWriter">Directed by:<span class="writer">{{movie.Director}}</span></h3>
            <h3 class="MovieWriter">Starring:<br><span class="writer">{{movie.Actors}}</span></h3>
            <button class="btn">Download</button>
          </div>
         
        </div>
      </div>
   
   
    </div>

</template>

<script> 
export default { 
   props:['movie'],
   
  data () {
    return {
        search:'',
        input:'', 

        
    }
  },
  methods: {
   submit() {
    this.$emit('submit', this.search)  
 }
}
}
</script>

<style scoped>
  .search {
    border-color: #E40808;
  }
  .movieName {
    font-family:sans;
    font-size: 40px;
    font-weight: 700;
  }
  .movieSub {
    font-size:15px;
  }
  .moviePlot {
    font-family:sans;
    font-size: 25px;
  }
  .MovieWriter {
    font-family:sans;
    font-size: 32px;
    font-weight: 300;
  }
  .writer {
    color:#726D6D;
    font-size:20px;
    font-family: sans;
  }
  .btn {
     background-color: #93020B;
     color:white;
  }
</style>
