<template>
	<li>{{ fullName }}</li>
</template>

<script>
export default {
	props: {
		user: Object,
	},
	computed: {
		fullName: function() {
			return this.user.firstName + " " + this.user.lastName
		},
	},
}
</script>
