<template>
	<el-card class="box-card">
		<div v-for="(value, key) in user" :key="value" class="text item">
			{{ key + ": " + value }}
		</div>
	</el-card>
</template>

<script>
export default {
	props: [`user`],
}
</script>

<style>
.text {
	font-size: 14px;
}

.item {
	padding: 18px 0;
}

.box-card {
	width: 480px;
}
</style>
