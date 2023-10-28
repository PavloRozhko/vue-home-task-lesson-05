<template>
	<div class="product-card">
		<div class="product-image">
			<img :src="productItem.imgSrc">
		</div>
		<div class="product-info">
			<div class="product-seller">
				<img :src="productItem.logo">
				<span>{{ productItem.companyTitle }}</span>
			</div>
			<div class="product-name">
				{{ productItem.description }}
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'ProductCard',
	props: {
		productItem: {
			type: Object,
			default: () => ({})
		},
	},
}
</script>

<style lang="css" scoped>
.product-card {
	display: flex;
	flex-direction: column;
	gap: 5px;
	justify-content: space-between;
	/* width: 150px; */
}

.product-image {
	width: 150px;
	height: 150px;
}

.product-image img {
	max-width: 100%;
}

.product-info {
	color: grey;
	display: flex;
	flex-direction: column;
	align-items: flex-start;
	gap: 5px;
}

.product-seller {
	font-size: 14px;
}

.product-name {
	font-size: 20px;
}
</style>