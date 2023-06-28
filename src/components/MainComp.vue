<script>
import {store} from '../store';
import SingleCard from './SingleCard.vue';

  export default{
    name: "MainComp",
    components: {
    SingleCard
  },
    data(){
      return{
        store
      }
    }
  }
</script>

<template>
  <div>
    <SingleCard v-for="(elem,index) in store.posts" :propsCard=elem />
  </div>
</template>

<style lang="scss" scoped>

</style>