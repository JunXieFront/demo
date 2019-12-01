<template name="labels">
	<view class="label">
		{{content}}
	</view>
</template>

<script>
	export default{
		name:'labels',
		props:['content']
	}
</script>
	
<style>
	.label{
		width:120rpx;
		height:40rpx;
		line-height: 40rpx;
		border:1rpx solid #999;
		color:#999;
		display: inline-block;
		margin-right:20rpx;
	}
</style>
