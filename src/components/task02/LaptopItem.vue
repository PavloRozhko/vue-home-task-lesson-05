<template>
	<div class="laptop-card">
		<div class="laptop-image">
			<img :src="laptopData.imgSrc">
		</div>
		<div class="laptop-info">
			<h3 class="laptop-title">{{ laptopData.title }}</h3>
			<div class="laptop-discount">
				Ваша економія:
				<span>{{ laptopData.discount }} ₴</span>
			</div>
			<div class="laptop-old-price"><span>{{ laptopData.oldPrice }}</span>₴</div>
			<div class="laptop-cta">
				<div class="laptop-price"><span>{{ laptopData.price }}</span>₴</div>
				<button class="laptop-btn">Купити</button>
			</div>
		</div>

	</div>
</template>

<script>
export default {
	name: 'LaptopItem',
	props: {
		laptopData: {
			type: Object,
			default: () => ({})
		},
	},
}
</script>

<style lang="css" scoped>
.laptop-card {
	display: flex;
	align-items: flex-start;
	gap: 15px;
	padding-bottom: 15px;
	border-bottom: 1px solid gray;
}

.laptop-image {
	width: 150px;
	height: 150px;
	flex: 0 1 auto;
}

.laptop-image img {
	max-width: 100%;
}

.laptop-info {
	display: flex;
	flex-direction: column;
	gap: 10px;
	text-align: left;
	flex-grow: 1;
}

.laptop-title {
	color: #6a96be;
	font-size: 24px;
	margin: 0;
}

.laptop-title:hover {
	text-decoration: underline;
}

.laptop-discount {
	font-size: 16px;
}

.laptop-discount span {
	color: red;
}

.laptop-old-price {
	color: #cdcccc;
}

.laptop-old-price span {
	font-size: 24px;
	position: relative;
}

.laptop-old-price span::after {
	content: '';
	position: absolute;
	top: 50%;
	left: 0;
	display: inline-block;
	height: 2px;
	width: 100%;
	background-color: #cdcccc;
}

.laptop-cta {
	display: flex;
	gap: 25px;
}

.laptop-price {
	color: #f8454a;
}

.laptop-price span {
	font-size: 32px;
}

.laptop-btn {
	color: #fff;
	padding: 10px 20px;
	border-radius: 5px;
	background-color: green;
	transition: background-color 0.3s ease 0s;
}

.laptop-btn:hover {
	background-color: #025a02;
}
</style>