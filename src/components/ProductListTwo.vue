<template>
    <div id="product-list-two">
        <h2>Product List Two</h2>
        <ul>
            <li v-for="(product,index) in saleProducts" v-bind:key="index">
                <span class="name">{{ product.name }}</span>
                <span class="price">£{{ product.price }}</span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  computed: {
    products () {
      return this.$store.state.products
    },
    saleProducts () {
      return this.$store.getters.saleProducts
    }
  }
}
</script>
