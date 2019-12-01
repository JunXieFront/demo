<template>
	<view>
		<banner :list="list"></banner>
		<view class="navto"><navto :list="list"></navto></view>

		<view class="com">
			<view class="text_good">优选</view>
			<view class="arrow"></view>
		</view>
		<listcontainer :list="con"></listcontainer>
	</view>
</template>

<script>
import navto from '../../component/navto/navto.vue';
import banner from '../../component/banner/banner.vue';
import listcontainer from '../../component/listcontainer/listcontainer.vue';
export default {
	data() {
		return {
			list: [
				{ src: '/static/img.jpg', text: 'aaa', id: '1', url: './' },
				{ src: '/static/img.jpg', text: 'aaa', id: '2', url: './' },
				{ src: '/static/img.jpg', text: 'aaa', id: '3', url: './' }
			],
			con:[
				{	
					id:'1',
					title:'天府三街 ',
					size:'10',
					side:'南',
					price:'1000',
					transport:'交通便利',
					floor:'1',
					src:"/static/icon/oldman.png",
					labels:["超值","超划算","超棒"]
				},
		{
			id:'1',
			title:'天府三街 ',
			size:'10',
			side:'南',
			price:'1000',
			transport:'交通便利',
			floor:'1',
			src:"/static/icon/oldman.png",
			labels:["超值","超划算","超棒"]
		},
		{
			id:'1',
			title:'天府三街 ',
			size:'10',
			side:'南',
			price:'1000',
			transport:'交通便利',
			floor:'1',
			src:"/static/icon/oldman.png",
			labels:["超值","超划算","超棒"]
		}
			]
		};
	},
	components: {
		navto,
		banner,
		listcontainer
	}
};
</script>

<style>
	.com{
		height: 60rpx;
		line-height: 60rpx;
		width: 750rpx;
		border-bottom: 1px solid #C0C0C0;
	}
.navto {
	margin-top: 10px;
	border-bottom: 1rpx solid #C0C0C0;
}
.text_good{
	color: #999999;
	font-size: 36rpx;
	float: left;
	margin-left: 15rpx;
}
.arrow{
	height:0;
	width: 0;
	border-top: 20rpx solid transparent;
	border-bottom: 20rpx solid transparent;
	border-left: 20rpx solid #2C405A;
	float: right;
	margin-right: 35rpx;
	margin-top: 10rpx;
}
</style>
