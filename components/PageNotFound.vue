<template>
    <div>
        <h1>Page Not Found</h1>
        <img :src="require('@/store/images/fe25.jpg')" alt="">
    </div>
</template>

<script>
import PageNotFound from '../components/PageNotFound.vue'
    export default {
        comments:{PageNotFound},
        
    }
</script>

<style scoped>
div {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50rem
}

h1 {
    font-size: 7.5rem;
}

img {
    width: 15rem;
    margin: 0 auto
}
</style>