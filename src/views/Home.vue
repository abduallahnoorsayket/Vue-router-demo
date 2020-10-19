<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <List/>
    <ComputedProps/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import List from '@/components/List.vue'
import ComputedProps from '@/components/ComputedProps.vue'

export default {
  name: 'Home',
  components: {
    List,
    ComputedProps
    
  }
}
</script>
