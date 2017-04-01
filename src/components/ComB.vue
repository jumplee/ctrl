<template>
  <div>

<div class="classB">B组件 <button @click="onClickB">改变一下C</button></div>

  </div>
</template>

<script>
import ctrl from './HelloCtrl'
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
    onClickB(){

      ctrl.trigger('changeC','改变C')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
