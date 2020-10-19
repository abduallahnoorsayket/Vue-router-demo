<template>
  <div class="computed">
    <h1>Computed Properties :</h1>
   <div>Enter price:
       <input type="text" v-model="price">
   </div>
   <div>Tax : {{tax }}</div>
   <div> Total : {{total }}</div>
  </div>
</template>

<script>
export default {
  name: 'ComputedProps',
  data:function() {

      return{
          price: 100,
      }
  },           
  computed: {
      tax: function(){
          return this.price * 0.2;
      },
      total:function(){
          return parseInt(this.price) + this.tax;

      }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.computed{
    margin-top:100px;
}
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
</style>
