<template>
  <div id="child1" class="component">
    
    <h2>Child 1 Component</h2>
    <span>{{message}}</span>
    <br/><br/>
    <button @click="changeMessage">Change Message</button>
  </div>
</template>

<script>
export default {
  props: {
    message:{String},
    changeMessage: Function
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#child1 {
  background-color: lightseagreen;
  
}
</style>
