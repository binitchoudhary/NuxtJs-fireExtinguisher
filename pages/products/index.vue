<template>
    <div>
        <Nav />
    <div class="container">
        <LargeCardDisplay 
        v-for="cardInfo in largeCardInfo.slice(0,1)" :key="cardInfo.id" 
        :cardsSection="cardInfo" 
        />
        <SmallCardDisplay 
        v-for="cardInfo in smallCardSections" :key="cardInfo.id" 
        :cardsSection="cardInfo" 
        />
    </div>
    </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/store/data.js"
import Nav from "../../components/Nav.vue";
export default {
    data() {
        return {
            largeCardInfo: largeCardSections,
            smallCardSections
        };
    },
    components: { Nav }
}
</script>

<style scoped>

</style>