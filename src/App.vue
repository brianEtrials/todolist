<template>
		<ToDoList msg="Hi Brian!">></ToDoList>
		<!-- <Time msg="The current time is "/> -->
</template>

<script>
import ToDoList from './components/ToDoList.vue'
// import Time from './components/Time.vue'

export default {
  name: 'App',
  components: {
	// Time,
	ToDoList,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
