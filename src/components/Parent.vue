<template>
  <div id="parent" class="component">
    
    <h2>Parent Component</h2>
    <span>{{msg}}</span>
      <hr/>
      <div class="row">
            <div class="col-xs-12 col-sm-6">
                <child1 :message="msg" :changeMessage="updateMessage"></child1>
            </div>
            <div class="col-xs-12 col-sm-6">
                <child2 :message="msg"></child2>
            </div>
      </div>
  </div>
</template>

<script>
import Child1 from './Child1.vue';
import Child2 from './Child2.vue';

export default {
  components:{child1:Child1, child2:Child2},
  data () {
    return {
      msg: 'Our lives begin to end the day we become silent about things that matter - Martin Luther King, Jr.'
    }
  },
  methods: {
    updateMessage(){
      this.msg = "A day of worry is more exhausting than a week of work - John Lubbock"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#parent {
  background-color: dodgerblue;
  
}



</style>
