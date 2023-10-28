<template>
	<div class="task-item">
		<h2>Задача № 2</h2>
		<products-panel :products-list="raspberryList" />
	</div>
</template>

<script>
import { raspberryList } from '@/constants/task01/data_raspberry'

import ProductsPanel from './ProductsPanel.vue'

export default {
	name: 'FirstTask',
	components: {
		ProductsPanel
	},
	data() {
		return {
			raspberryList
		}
	},
}
</script>

<style lang="css" scoped>
.task-item {
	padding-bottom: 15px;
	border-bottom: 2px solid #000;
}
</style>