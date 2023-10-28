<template>
	<div class="laptops-list">
		<laptop-item v-for="laptop in laptopsList" :key="laptop.id" :laptop-data="laptop" />
	</div>
</template>

<script>
import LaptopItem from './LaptopItem.vue'

export default {
	name: 'LaptopsPanel',
	components: {
		LaptopItem,
	},
	props: {
		laptopsList: {
			type: Array,
			default: () => []
		},
	},
}
</script>

<style lang="css" scoped>
.laptops-list {
	display: flex;
	flex-direction: column;
	gap: 25px;
}
</style>