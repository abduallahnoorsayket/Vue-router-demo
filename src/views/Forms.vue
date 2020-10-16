<template>
  <div class="about">
    <h1>This is an about page</h1>
    <SimpleForms/>
  </div>
</template>

<script>
// @ is an alias to /src
import SimpleForms from '@/components/SimpleForms.vue'

export default {
  name: 'Forms',
  components: {
    SimpleForms
  }
}
</script>
