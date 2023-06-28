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
            <div>
                <h6>TYPE</h6>
                <span>{{ propsCard.type }}</span>
            </div>
            <div>
                <h6>TECHNOLOGIES</h6>
                <span v-for="(elem,index) in propsCard.technologies">{{ elem.name }}</span>
            </div>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>