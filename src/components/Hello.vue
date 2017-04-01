<template>
  <div class="hello">
 <ComA />
  <ComB/>



  </div>
</template>

<script>
import ComA from './ComA'
import ComB from './ComB'
import ctrl from './HelloCtrl'



export default {
  name: 'hello',
    components:{
      ComA,ComB
  },
  data () {
    return {
      msg: '默认Hello'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.classA,.classB{
  padding:15px;
  background: lightblue;
  margin:15px;
}
.classB{
  background: lightpink;
}
</style>
