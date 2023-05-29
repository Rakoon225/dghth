<template>
	<div>
		<form class="app-form" @submit.prevent>
			<h4>Создать блок</h4>

			<my-input placeholder="Название" v-model="post.title"></my-input>

			<my-input placeholder="Описание" v-model="post.body"></my-input>

			<myButton class="btn" @click="createPost">Создать</myButton>
		</form>
	</div>
</template>
<script>
export default {
	data() {
		return {
			post: {
				title: '',
				body: '',
			}
		}
	},
	methods: {
		createPost() {
			this.post.id = Date.now();
			this.$emit('create', this.post);
			this.post = {
				title: '',
				body: '',
			}


		},
	}
}
</script>
<style lang="scss" scoped>
.app-form {
	display: flex;
	flex-direction: column;
	gap: 20px;

	max-width: 900px;
}
</style>