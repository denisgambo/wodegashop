<template>
  <div class="container">
    <di v-for="categorie in categories" :key="categorie.id">
      <p>{{ categorie.id }}: {{ categorie.catName }}</p>
    </di>

   </div>
</template>

<script>
export default {
  componet: {

  },

  data(){
    return {
      categories: [
        {id: 1, catName: 'cat1'},
        {id: 2, catName: 'cat2'}
      ]
    }
  }

}
</script>

<style>

</style>