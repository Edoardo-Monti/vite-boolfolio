<script >
import {store} from '../store'
import MainComp from '../components/MainComp.vue';
import axios from 'axios';

export default{
  name: 'PostList',
  components: {
    MainComp,
  },
  data(){
    return{
      store,
    }
  },
  mounted(){
    this.getPosts();
  },
  methods:{
    getPosts(){
      axios.get('http://127.0.0.1:8000/api/posts').then(res => {
        
        store.posts = res.data.posts
        // console.log(store.posts)
      })
    }
  }
}

</script>

<template>
  <div>
    <h1 class="animate__animated animate__rubberBand">Posts</h1>
    <MainComp/>
  </div>
</template>

<style lang="scss">
@use "../style/main.scss";
.animate__animated.animate__rubberBand{

    animation-delay: 2s;
}
h1{
  color: red;
}
</style>