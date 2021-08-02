<template>
	<div id="app">
		<ul>
			<li :key="user.id" v-for="user in users">{{ user.firstName }}</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: "App",
	data() {
		return {
			users: [
				{
					id: 1,
					firstName: "Dmytro",
					secondName: "Petrenko",
					position: "Trainee Vue Js Developer",
				},
				{
					id: 2,
					firstName: "Valeriy",
					secondName: "Nosenko",
					position: "Trainee React Js Developer",
				},
				{
					id: 3,
					firstName: "Andriy",
					secondName: "Parkhomenko",
					position: "Senior Vue Js Developer",
				},
				{
					id: 4,
					firstName: "Artemon",
					secondName: "Bulangery",
					position: "Designer",
				},
			],
		}
	},
	components: {},
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
