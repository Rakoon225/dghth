<template>
	<input type="text" class="inp">
</template>
<script>
export default {
	name: 'my-input',
}
</script>
<style lang="scss" scoped>
.inp {
	max-width: 100%;
	padding: 10px 15px;
	border: 2px solid teal;
	color: teal;
	transition: 200ms;
	cursor: pointer;
	border-radius: 5px;

	&::placeholder {
		color: darkslategray;
	}
}
</style>