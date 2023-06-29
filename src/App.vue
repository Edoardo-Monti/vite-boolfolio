<script >
import {store} from './store'
import AppHeader from './components/AppHeader.vue'

export default{
  name: 'App',
  components: {
    AppHeader,
  },
  
}

</script>

<template>
    <AppHeader/>
    <router-view/>
</template>

<style lang="scss">
@use "./style/main.scss";
.animate__animated.animate__rubberBand{

    animation-delay: 2s;
}
h1{
  color: red;
}
</style>
