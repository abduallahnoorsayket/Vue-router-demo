<template>
  <div>
    <p v-text="dropdownResult"></p>
   <dropdown @update:option="optionUpdate"></dropdown>
  </div>
</template>

<script>
import Dropdown from './Dropdown'
export default {
  name: 'List',
  components:{
      Dropdown
  },
 data: function(){
     return{
         dropdownResult:'',
     }
 },
 
  methods:{
      optionUpdate: function(value){
          this.dropdownResult = value;
      }

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
</style>
