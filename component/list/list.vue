<template name="indexlist">
<navigator :url="to">
	<view class="content">
		<!-- 图片的容器 -->
		<view class="img-cantainer">
			<image :src="imgsrc"/>
		</view>
		<!-- 文字内容的容器 -->
		<view class="text-container">
			<view class="title">{{title}}</view>
			<view class="description">
				<span>{{side}}</span>
				<span>|</span>
				<span>{{size}}</span>
				<span>|</span>
				<span>{{floor}}层</span>
			</view>
			<view class="transport">{{transport}}</view>
			<view class="labels">
				<labels v-for="(item,index) in labels" :key="index" :content="item"/>
			</view>
				<view class="price" >{{price}}/月 </view>
		</view>
	</view>
	</navigator>
</template>

<script>
	import labels from '../label/label.vue'
	export default{
		name:"indexlist",
		props:{
			to:{
					type:String,
					value:''
			},
			floor:{
					type:String,
					value:''
			},
			side:{
					type:String,
					value:''
			},
			size:{
					type:String,
					value:''
			},
			imgsrc:{
				type:String,
				value:''
			},
			title:{
				type:String,
				value:''
			},
			transport:{
				type:String,
				value:''
			},
			price:{
				type:Number,
				value:0
			},
			labels:{
				type:Array,
				value:[]
			},

		},

		components:{
			labels
		}
}
</script>

<style>
	.content{
		width:750rpx;
		padding:30rpx;
		font-size: 28rpx;
		color:#999;
		display: flex;
		flex-direction: row;
		height:200rpx
	}
	.content .img-cantainer{
		width:260rpx;
		height:100%;
		margin-right:10rpx;
	}
	.content .img-cantainer image{
		width:100%;
		height:100%;
	}
	.content .text-container{
		flex:1;
		height:260rpx;
		display: flex;
		flex-direction: column;
	}
	.content .text-container .title{
		color:#000;
		height:80rpx;
		line-height:80rpx;
	}
	.content .description,.content .transport{
		height:20rpx;
		line-height:20rpx;
		flex:1
	}
	.content .description{
		margin-left: -5rpx;
	}
	.content .description span{
		margin-left:10rpx
	}
	.content .price{
		color:#f40;
		font-size:36rpx;
		position: relative;
		bottom:-10rpx;
		height:40rpx;
		line-height:40rpx;
	}
</style>
