<template>
    <div class="container">
        <NuxtLink to="/">Go Back</NuxtLink>
        <div>
           <MyItem 
           v-for="item in myRentals"
           :key="item.id"
           :item="item"
           />
        </div>
    </div>
   
</template>

<script>
import {mapState} from 'vuex'
import MyItem from '../components/MyItem.vue'
export default {
    layout: "no-nav",
    computed: {
        ...mapState(["myRentals"])
    },
    components: { MyItem }
}
</script>

<style scoped>
.container {
    padding: 5rem 0;
}
</style>