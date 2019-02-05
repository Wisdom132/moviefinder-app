<template> 
<div>
<nav class="navbar navbar-light mynav">
 <div class="container">
  <span class="navbar-brand mb-0 text-light">Navbar</span>
  </div>
</nav>

</div>
</template>

<script> 

export default {
   props:['movie' ,'filteredBlogs'], 
  data () {
    return {
     
    }
  },
       
  methods: {
   
  },
}
</script>

<style scoped>
 .mynav {
   background-color:#93020B;
 }
</style>