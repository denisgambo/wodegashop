<template>
    <div class="container">
        <div v-for="td in todos" :key="td.id">
            {{ td }}
        </div>
    </div>
  
</template>

<script>
export default {
    name:'TodoCompnent',
    props: {
        todos: []
    }
}
</script>

<style scoped>
.container{
    text-align: center;
    justify-content: center;
}

</style>