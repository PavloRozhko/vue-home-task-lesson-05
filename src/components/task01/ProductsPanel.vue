<template>
	<div class="products-list">
		<product-card v-for="product in productsList" :key="product.id" :product-item="product" />
	</div>
</template>

<script>
import ProductCard from './ProductCard.vue'
export default {
	name: 'ProductsPanel',
	components: {
		ProductCard
	},
	props: {
		productsList: {
			type: Array,
			default: () => []
		},
	},
}
</script>

<style lang="css" scoped>
.products-list {
	display: flex;
	gap: 25px;
}
</style>