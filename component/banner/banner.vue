<template name="banner">
<!-- 	<view class="uni-padding-wrap">
		<view class="page-section swiper"> -->
			<view class="page-section-spacing">
				<swiper class="swiper" indicator-dots="true" autoplay="true" interval="2000" duration="500">
					<swiper-item v-for="item in list" :key="item.id">
						<view class="swiper-item"><image :src="item.src"></image></view>
					</swiper-item>
				</swiper>
			</view>
<!-- 		</view>
	</view> -->
</template>

<script>
	export default{
		name:'banner',
		props:["list"]
	}
</script>

<style>
</style>
