<template>
	<div class="post">
		<div>
			<div><strong>Название: </strong> {{ post.title }} </div>
			<div><strong>Описание: </strong> {{ post.body }} </div>
		</div>
		<div class="post__btns">
			<my-btn class="btn-delete btn">Удалить</my-btn>
		</div>
	</div>
</template>
<script>
export default {
	props: {
		post: {
			type: Object,
			required: true,
		}
	}
}
</script>
<style lang="scss" scoped>
.post {
	display: flex;
	justify-content: space-between;
	align-items: center;
	max-width: 900px;
	margin-top: 20px;

	padding: 20px;
	border: 2px solid teal;
	border-radius: 5px;
}

.btn-delete {
	padding: 10px 12px;
	font-size: 15px;
}
</style>