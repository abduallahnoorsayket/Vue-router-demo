<template>
  <div class="about">
    <h1>This is an about page</h1>
    <SkipLink/>
  </div>
</template>

<script>
// @ is an alias to /src
import SkipLink from '@/components/SkipLink.vue'

export default {
  name: 'About',
  components: {
    SkipLink
  }
}
</script>
