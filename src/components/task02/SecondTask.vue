<template>
	<div class="task-item">
		<h2>Задача № 3</h2>
		<laptops-panel :laptops-list="notebooksList" />
	</div>
</template>

<script>
import LaptopsPanel from './LaptopsPanel.vue'
import { notebooksList } from '@/constants/task02/data_notebooks'
export default {
	name: 'SecondTask',
	components: {
		LaptopsPanel,
	},
	data() {
		return {
			notebooksList
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