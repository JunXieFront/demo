<template name="nav">
	<view id="component" class="root">
		<view v-for="(item, index) in list" :key="list.id">
			<navigator :url="item.url">
				<img :src="item.src" class="img" />
				<view class="text">{{ item.text }}</view>
			</navigator>
		</view>
	</view>
</template>

<script>
export default {
	name: 'nav',
	props: ['list'],
	created: function(e) {},
	methods: {}
};
</script>

<style>
.img {
	height: 20px;
	width: 20px;
	text-align: center;
	background-color: #007aff;
	margin-left: 3.5px;
	vertical-align: middle;
	
}
.root {
	height: 50px;
	width: 100%;
	display: flex;
	flex-direction: row;
	justify-content: space-around;
}
.text {
	height: 20px;
	width: auto;
	
	line-height: 20px;
	font-size: 16px;
}
</style>
