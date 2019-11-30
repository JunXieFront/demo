<template>
	<view><navto :list="list"></navto></view>
</template>

<script>
import navto from '../../component/navto.vue';
export default {
	data() {
		return {
			list: [
				{ src: 'img.jpg', text: 'aaa', id: '1', url: './' },
				{ src: 'img.jpg', text: 'bbb', id: '2', url: './' },
				{ src: 'img.jpg', text: 'ccc', id: '3', url: './' },
				{ src: 'img.jpg', text: 'ccc', id: '3', url: './' },
				{ src: 'img.jpg', text: 'ccc', id: '3', url: './' }
			]
		};
	},
	components: {
		navto
	}
};
</script>

<style></style>
