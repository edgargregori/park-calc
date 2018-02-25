<template>
  <div id="app">
    <parking>
    </parking>
    <mypicker>
    </mypicker>
  </div>
</template>

<script>
import Vue from 'vue'
import Mypicker from './components/datepicker/Mypicker'
import Parking from './components/parking/Parking'
Vue.component('parking', function (resolve) { require(['./components/parking/Parking.vue'], resolve) })
Vue.component('Mypicker', function (resolve) { require(['./components/datepicker/Mypicker.vue'], resolve) })
export default {
  name: 'app',
  component: { Mypicker, Parking }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
