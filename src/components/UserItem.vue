<template>
	<li @click="onClick">{{ fullName }}</li>
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
	methods: {
		onClick() {
			this.$emit(`setCurrentUser`, this.user)
		},
	},
}
</script>
