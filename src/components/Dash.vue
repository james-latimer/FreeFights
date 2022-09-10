<template>
  <div class="care">
    <Carousel/>
  </div>
</template>

<script>
  /* eslint-disable */ 
import Carousel from './Carousel.vue'
export default {
  name: 'Dash',
  components: {
    Carousel
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
} */
/* video{
  height: 150px;
  width: 1;
} */
.care{
  margin: 50px;
}
</style>
