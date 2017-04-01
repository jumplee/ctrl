<template>
  <div class="classC">
C组件 {{msg}}
  </div>
</template>

<script>
import ctrl from './HelloCtrl'
export default {
  name: 'hello',
  created(){
    var self=this
    ctrl.bind('changeC',function(msg){
      self.msg=msg+ctrl.counter
      console.log(ctrl)
      ctrl.counter++
    })
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.classC{
  border:1px solid;
  color:white;
}
</style>
