<template>
  <div id="app">
    <h1>Parent: {{ carName }}</h1>
    <app-car 
      v-bind:carName="carName"
      v-bind:carYear="carYear"
    ></app-car>
  </div>
</template>

<script>
import Car from './Car.vue'

export default {
  name: 'app',
  data() {
    return {
      carName: 'Ford from parent',
      carYear: '2018'
    }
  },
  components: {
    appCar: Car
  }
}
</script>