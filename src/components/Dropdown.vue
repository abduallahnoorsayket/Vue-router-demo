<template>
  <select name="dropdown" id="dropdown" v-model="selectedOption" @change="optionChanged">
      <option value="null" disabled> please select an option </option>
      <option value="Php"> Php</option>
      <option value="Pyhton"> Pyhton</option>
      <option value="java"> java</option>
  </select>
</template>

<script>
export default {
  name: 'Dropdown',
  data:function(){
      return {
          selectedOption:null,
      }
  },
  
  methods:{
     optionChanged: function(){
         this.$emit('update:option', this.selectedOption)
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
