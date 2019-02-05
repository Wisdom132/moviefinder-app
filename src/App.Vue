<template> 
  <div>
  <movie></movie>
  <search :movie='movie' @submit='finished($event)'></search>
  <my-footer></my-footer>

  </div>
</template>

<script> 
const key = '17de97b1';
const defaultTitle = 'rampage';
const url = `http://www.omdbapi.com/?i=tt3896198&apikey=17de97b1&t=`;

import movie from './components/movie.vue'
import search from './components/search.vue'
import footer from './components/footer.vue'
export default {
  components: {
    'movie': movie, 
    'search': search,
    'my-footer':footer
  },
  data () {
    return {
     movie: {},
     search: '',
     title:'',
     input:'',
     url:'http://www.omdbapi.com/?i=tt3896198&apikey=17de97b1&t=',
    }
  },
   created(){
    this.fetchData(defaultTitle);
  },
 
  
  methods: {
    fetchData: function (input) {
      this.$http.get(url + input)
      .then(function(data){
      this.movie = data.body;
      console.log(data);        
}).catch(err => {
        console.log(error);
      });
},
  finished(updated) {
    let input= this.$refs = updated; 
    console.log(input);
     if (updated) {
        this.fetchData(updated);

    }
},
}
}
</script>

<style scoped>

</style>
