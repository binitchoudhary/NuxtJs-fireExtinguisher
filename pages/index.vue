<template>
  <div>
    <Nav />
<div class="container">
    <Hero />
    <LargeCardDisplay 
    v-for="cardInfo in largeCardInfo" 
    :key="cardInfo.id"
    :cardsSection ="cardInfo"
    />
    <SmallCardDisplay 
     v-for="cardInfo in smallCardSections" 
    :key="cardInfo.id"
    :cardsSection ="cardInfo"
    />
</div>
</div>
</template>

<script>
import { largeCardSections, smallCardSections } from '../store/data.js'
import Hero from '../components/Hero.vue';
import LargeCardDisplay from '../components/LargeCardDisplay.vue';
import SmallCardDisplay from '../components/SmallCardDisplay.vue';
import Nav from '../components/Nav.vue';

export default {
    name: "IndexPage",
    components: { Hero, LargeCardDisplay, SmallCardDisplay, Nav },
    data(){
      return{
        largeCardInfo: largeCardSections,
        smallCardSections
      }
    }
}
</script>
