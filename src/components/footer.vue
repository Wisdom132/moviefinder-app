<template> 
<div>
    <div class="container-fluid myfooter">
        <div class="row">
            <div class="col-md-12">
                	<h6 class="copy mt-2">&copy;copyright 2018 Wisdom Ekpot</h6>

            </div>
        </div>
    </div>

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
 .myfooter {
   background-color:#93020B;
   height:40px;
 }
 .copy {
     text-align: center;
     color:#ffffff;
 }
</style>