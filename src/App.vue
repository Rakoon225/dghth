<template>
	<div class="app">
		<PostForm @create="createPost" />
		<PostList :posts="posts" />
	</div>
</template>

<script>

import PostForm from '@/components/PostForm.vue';
import PostList from '@/components/PostList.vue';

export default {
	components: { PostList, PostForm },
	data() {
		return {
			posts: [
				{ id: 1, title: 'JavaScript', body: `Описание поста 1` },
				{ id: 2, title: 'Python', body: `Описание поста 2` },
				{ id: 3, title: 'C++', body: `Описание поста 3` },
				{ id: 4, title: 'Jquery', body: `Описание поста 4` },
			],
		}
	},
	methods: {
		createPost(post) {
			this.posts.push(post);
		}
	}
}
</script>

<style lang="scss">
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	font-family: 'Courier New', Courier, monospace;
}

.app {
	margin: 50px 70px;
}
</style>