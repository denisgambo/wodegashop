<template>
  <div class="container">
    <FromChildToParent @clothes="getClothes"/>
    <h1>Nos produits</h1>
    <div v-for="pr in prod" :key="pr.id" class="card">
      <div class="card-header">
        <h2 class="card-title">{{ pr.name }}</h2>
      </div>
      <div class="card-body">
        <div class="card-texts">
          <p>{{ pr.price }}£</p>
        </div>
      </div>
    </div>
  </div>
  
</template>

<script>
import FromChildToParent from '../components/FromChildToParent.vue'
export default {
  name: 'ClothesView',
  data(){
    return {
      prod: []
    }
  },
  methods: {
    getClothes(clothe){
      this.prod = clothe
    }
  },
  components: {
    FromChildToParent
  }
}
</script>

<style>

</style>