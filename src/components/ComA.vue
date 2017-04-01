<template>
  <div class="hello">
    <div class="classA">
      {{msg}}
      <ComC></ComC>
    </div>

  </div>
</template>

<script>
import ctrl from './HelloCtrl'
import ComC from './ComC'
export default {
  name: 'hello',
  components:{
    ComC
  },
  created(){
    var self=this
    ctrl.bind('changeA',function(msg){
      self.msg=msg
    })
  },
  data () {
    return {
      msg: 'A组件原始数据'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
