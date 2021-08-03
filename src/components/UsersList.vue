<template>
	<ul>
		<transition-group name="userList">
			<UserItem v-bind:user="user" :key="user.id" v-for="user in users" />
		</transition-group>
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
.userList-enter-active {
	transition: all 1s;
}
.userList-enter /* .userListleave-active до версии 2.1.8 */ {
	opacity: 0;
	transform: translateY(30px);
}
</style>
