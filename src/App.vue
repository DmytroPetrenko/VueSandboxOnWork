<template>
	<div id="app">
		<UsersList v-bind:users="users" />
		<AddNewUser @add-new-user="addNewUser" />
		<CustomInput v-model="customInputText" />
		{{ customInputText }}
	</div>
</template>

<script>
import UsersList from "@/components/UsersList"
import AddNewUser from "@/components/AddNewUser"
import CustomInput from "@/components/CustomInput"

export default {
	name: "App",
	data() {
		return {
			users: [
				{
					id: 1,
					firstName: "Dmytro",
					lastName: "Petrenko",
					position: "Trainee Vue Js Developer",
				},
				{
					id: 2,
					firstName: "Valeriy",
					lastName: "Nosenko",
					position: "Trainee React Js Developer",
				},
				{
					id: 3,
					firstName: "Andriy",
					lastName: "Parkhomenko",
					position: "Senior Vue Js Developer",
				},
				{
					id: 4,
					firstName: "Artemon",
					lastName: "Bulangery",
					position: "Designer",
				},
			],
			customInputText: "",
		}
	},
	components: {
		UsersList,
		AddNewUser,
		CustomInput,
	},
	methods: {
		addNewUser(newUser) {
			this.users.push(newUser)
		},
	},
}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
