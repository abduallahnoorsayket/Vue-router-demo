<template>
  <div class="demo">
  <!-- Skip Links -->
  <a href="#main" class="skipLink" ref="skipLink"></a>

  <main tabindex="-1" id='main'>
    <h1>First  content</h1>
    <p>Tab to move to the navbar.</p>
    
  </main>
  <main tabindex="-1" id='main'>       
     <h1>Second  content</h1>
    <p>Tab to move to the navbar.</p>
  </main>

  <main tabindex="-1" id='main'>       
     <h1>Third   content</h1>
    <p>Tab to move to the navbar.</p>
  </main>

<main tabindex="-1" id='main'>       
     <h1>fourth  content</h1>
    <p>Tab to move to the navbar.</p>
  </main>
  </div>
</template>

<script>
export default {
  watch: {
    $route() {
      this.$refs.skipLink.focus();
    }
  }
};
</script>

<style>
.demo {
  font-family: sans-serif;
  border: 1px solid #eee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}

#main {
  margin: 3em auto
}

.skipLink {
  white-space: nowrap;
  margin: 1em auto;
  top: 0;
  position: fixed;
  left: 50%;
  margin-left: -72px;
  opacity: 0;
}

.skipLink:focus {
  opacity: 1;
  background-color: white;
  padding: .5em;
  border: 1px solid black;
}
  
</style>