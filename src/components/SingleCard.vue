<script>
export default{
    name:"SingleCard",
    props:['propsCard']
}

</script>

<template>

    <div v-if="(propsCard.image)" class="card" style="width: 18rem;">
        <img  :src="`http://127.0.0.1:8000/storage/${propsCard.image}`" class="card-img-top" alt="">
        <div class="card-body">
            <h5 class="card-title">{{ propsCard.title }}</h5>
            <p class="card-text">{{ propsCard.description }}</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>