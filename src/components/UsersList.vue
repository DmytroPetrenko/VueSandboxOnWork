<template>
	<ul>
		<UserItem v-bind:user="user" :key="user.id" v-for="user in users" />
	</ul>
</template>

<script>
import UserItem from "@/components/UserItem"
export default {
	props: ["users"],
	components: { UserItem },
}
</script>

<style>
ul {
	list-style-type: none;
}
</style>
