<script>
export default {
    props: {
        product: {
            type: Object,
            required: true
        }
    },
    methods: {
        addToCart() {
            this.$emit('add-to-cart', this.product)
        }
    }
}
</script>

<template>
    <button class="btn btn-success" @click="addToCart">Añadir al Carrito</button>
</template>

<style scoped>

</style>