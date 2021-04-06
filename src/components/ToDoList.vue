<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>

  <form>
	<label>TODO</label>
	<input v-model="newTodo" type="text"/>
	<!-- remember v-model is like value and input -->
	<button @click="addTodo" type="button">Add</button>
  </form>
  <ul>
	<li v-for="(item, index) in todos" :key="index">
		{{item}}
		<button @click="deleteTodo(index)">delete</button>
	</li>
  </ul>
</template>

<script>
export default {
	props:{
		msg: String,
	},
	data: function(){
		return{
			newTodo: '',
			todos: [],
		}
	},
	methods: {
		addTodo(){
			console.log('clicked add');
			if(this.newTodo.length === 0) {
				console.log('Enter something')
			}
			else {
				this.todos.push(this.newTodo);
			}
		},
		deleteTodo(item){
			this.todos.splice(item, 1);
		}
	}
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
