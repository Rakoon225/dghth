<template>
	<div class="posts-container">
		<h3>Список записей</h3>
		<post-item :post="post" v-for="post in posts" />
	</div>
</template>

<script>
import PostItem from '@/components/PostItem.vue';
export default {
	components: { PostItem },
	props: {
		posts: {
			type: Array,
			required: true,
		}
	}
}
</script>

<style lang="scss" scoped>
.posts-container {
	margin-top: 50px;
}
</style>