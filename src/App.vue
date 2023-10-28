<template>
	<first-task />
	<second-task />
</template>

<script>
import FirstTask from './components/task01/FirstTask.vue';
import SecondTask from './components/task02/SecondTask.vue'
export default {
	name: 'App',
	components: {
		FirstTask,
		SecondTask
	}
}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	max-width: 1200px;
	margin: 0 auto;
	/* -webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px; */
}
</style>
