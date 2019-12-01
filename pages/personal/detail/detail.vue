<template>
	<!-- party界面 -->
	<view>
		<view class="uni-padding-wrap">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
						<swiper-item>
							<view class="swiper-item"><image src="../../../static/img.jpg"></image></view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item"><image src="../../../static/img.jpg"></image></view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item"><image src="../../../static/img.jpg"></image></view>
						</swiper-item>
					</swiper>
				</view>
			</view>
		</view>
		<!-- 轮播图下方 -->
		<view style="border-top: 1px solid #808080; margin-top: 3px;border-bottom: 1px solid #C0C0C0;">
			<view class="title" style="display: flex;">
				<image src="../../../static/order.png" style="width: 20px;height: 20px;margin-left: 5px;margin-top: 5px; "></image>
				<view style="margin-left: 10px;font-size: 12px;margin-top: 7px;font-weight: bold;">青年火锅party，热辣火爆，让你吃喝玩到嗨</view>
			</view>
			<view class="other"><span style="font-size: 10px; color: #808080;margin-left: 10px;">Part·南 | 约 19m2 | 10/19层</span></view>
			<view class="label" style="font-size: 10px; font-weight: bold;margin-top: 10px;padding-bottom: 10px;">
				<span style="color: #4CD964;margin-left: 5px;">√ 可预约</span>
				<span style="color: #4CD964;margin-left: 5px;">√ 可带酒水</span>
				<span style="color: #f40;margin-left: 5px;">√ 不可退款</span>
			</view>
		</view>
		<!-- 注意事项 -->
		<view>
			<h6 style="font-weight: bold;display: flex;justify-content: center;margin-top: 10px;">注意事项</h6>
			<!-- <view style="height: 2px;width: 15px; display: flex;justify-content: center;background-color: yellow;"></view> -->
			<view class="content" style="width: 90%;margin: 0 auto;">
				<view style="color: red;font-size: 12px;font-weight: bold;margin-top: 15px;">套餐包含</view>
				<view class="meal">菌菇拼盘(四种类型)*1份 68元</view>
				<view class="meal">蔬菜拼盘（豌豆 番茄 土豆 豆皮 玉米）*1份 25元</view>
				<view class="meal">素菜手工菜拼盘（品种随季节变化）*1份 3元</view>
			</view>
		</view>
		<!-- 配置 -->
		<view style="margin-top: 15px;border-top: 1px solid #C8C7CC;">
			<span
				style="font-weight: bold;font-size: 14px;margin-left: 10px;margin-top: 5px;border-bottom: 1px solid black
			;"
			>
				卧室配置
			</span>
			<span style="font-size: 13px;margin-left: 10px;margin-top: 15px;">公共配置</span>
		</view>
		<view style=" display: flex; justify-content: space-around;margin-top: 10px;">
			<image src="../../../static/bed.png" style="height:20px; width:20px"></image>
			<image src="../../../static/chest.png" style="height:20px; width:22px;margin-left: -5px;"></image>
			<image src="../../../static/desk.png" style="height:20px; width:20px"></image>
			<image src="../../../static/air.png" style="height:20px; width:20px"></image>
		</view>
		<view style="display: flex; justify-content: space-around; font-size: 12px; margin-left: 5px;">
			<span>床</span>
			<span>衣柜</span>
			<span>书桌</span>
			<span>空调</span>
		</view>
		<view style="margin-top: 10px;border-top: 1px solid #C8C7CC;"><view style="font-size: 14px; font-weight: bold;margin-left: 10px; margin-top: 5px;">小区及周边</view></view>
		<view style="display: flex;margin-left: 10px; margin-top: 10px;">
			<view style="color: blue; border-bottom: 1px solid blue;font-size: 14px;width: 35px;text-align: center;">交通</view>
			<view style="color: #808080; margin-left: 10px;font-size: 14px;">商场</view>
		</view>
		<view><map style="width: 100%; height: 200px;margin-top: 10px;margin-bottom: 10px;" :latitude="latitude" :longitude="longitude" :markers="covers"></map></view>
		<view style="border-top: 1px solid #C8C7CC;">
			<view style="color: #808080;font-size: 14px; margin-top: 10px; margin-bottom: 10px; margin-left: 10px; font-weight: bold;" >其他 Part</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			background: ['color1', 'color2', 'color3'],
			indicatorDots: true,
			autoplay: true,
			interval: 2000,
			duration: 500,

			title: 'map',
			latitude: 39.909,
			longitude: 116.39742,
			covers: [
				{
					latitude: 39.909,
					longitude: 116.39742,
					iconPath: '../../../static/location.png'
				},
				{
					latitude: 39.9,
					longitude: 116.39,
					iconPath: '../../../static/location.png'
				}
			]
		};
	},
	methods: {
	}
};
</script>

<style>
.meal {
	color: #999999;
	font-size: 12px;
	line-height: 15px;
	height: 15px;
	margin-top: 5px;
}
</style>
