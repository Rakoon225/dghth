<template>
	<button class="btn">
		<slot></slot>
	</button>
</template>
<script>
export default {
	name: 'btn',
}
</script>
<style lang="scss" scoped>
.btn {
	display: flex;
	justify-content: center;
	align-items: center;

	background-color: teal;
	color: aliceblue;
	padding: 10px 15px;
	border-radius: 5px;
	max-width: 150px;
	border: none;
	cursor: pointer;

	transition: 200ms;

	&:hover {
		background-color: darkslategrey;
	}

	&:active {
		background-color: green;
	}
}
</style>