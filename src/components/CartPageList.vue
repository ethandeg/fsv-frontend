<template>
    <div v-if="cartItems.length > 0">
        <CartItem v-for="product in cartItems" :key="product.id" :product="product"/>
    </div>
    <p v-else>You haven't added anything to your cart yet.</p>
</template>


<script>
    import CartItem from "./CartItem.vue"
    export default {
        name: "CartPageList",
        props: ['cartItems'],
        components: {
            CartItem,
        }
    }
</script>


