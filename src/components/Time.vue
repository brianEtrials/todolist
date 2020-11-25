<template>
	<div>

		<h1>{{ msg }}{{ timestamp }}</h1>
	</div>
</template>

<script>
export default {
	props: {
		msg: String
	},
	data: function() { 
		return {
			timestamp: "",
		} 
	},
	created() {
			setInterval(this.getNow, 1000);
		},
	methods: {
			getNow: function() {
				const today = new Date();
				const date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();
				const time = today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
				const dateTime = date +' '+ time;
				this.timestamp = dateTime;
			}
		}
}
</script>