<template>
  
</template>

<script>
export default {
    name:'FromChildToParent',
    data(){
        return {
            products: [
                {id:1, name: "shoes", price: 15},
                {id:2, name: "shirt", price: 30},
                {id:3, name: "pants", price: 20},
            ]
        }
    },
    methods: {
        sellClothes(){
            this.$emit("clothes", this.products)
        }
    },
    mounted(){
        this.sellClothes()
    }

    //send the products list to ClothesView

}
</script>

<style>

</style>