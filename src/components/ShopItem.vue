<template>
    <div class="item">
        <router-link :to="/shop/ + product.id">
            <img class="item-img" :src="product.img" :alt="product.title">
            <p class="item-title"> {{ product.title }} </p>
        </router-link>
    </div>
</template>

<script>
export default {
    props: {
        product: {
            type: Object,
            required: true
        }
    }
}
</script>

<style lang="scss">
    .item__wrapper{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
    }
    .item {
        max-width: 48%;
        text-align: center;
        &-title {
            font-size: 22px;
        }
        &-img {
            width: 70%;
            margin: 0px auto;
        }
    }
</style>