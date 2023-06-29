<script>
export default{
    name:"SingleCard",
    props:['propsCard']
}

</script>

<template>

    <div class="card" style="width: 18rem;">
        <img  :src="`http://127.0.0.1:8000/storage/${propsCard.image}`" class="card-img-top" alt="">
        <div class="card-body">
            <h5 class="card-title">{{ propsCard.title }}</h5>
            <p class="card-text">{{ propsCard.description }}</p>
            <div>
                <h6>TYPE</h6>
                <span>{{ propsCard.type }}</span>
            </div>
            <div>
                <h6>TECHNOLOGIES</h6>
                <span v-for="(elem,index) in propsCard.technologies">{{ elem.name }}</span>
            </div>
            <router-link :to="{name: 'SinglePost', params: {slug: propsCard.slug}}" class="btn btn-primary">
                Visita Pagina Dedicata
            </router-link>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>