<template>
  
</template>

<script>
export default {
    name:'NewProductForm',
    data(){
        return {
            newproduct:{
                id:1,
                name:'',
                price:0,
                img:''
            }
        }
    },
    methods: {
        addProduct(product){
            this.products.push(product)
        }
    }

}
</script>

<style>

</style>