<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Products-list/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import ProductsList from '@/components/ProductsList.vue'

export default {
  name: 'HomeView',
  components: {
    // HelloWorld
    ProductsList
  }
}
</script>
