<template>
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
				<view style="margin-left: 10px;font-size: 12px;margin-top: 7px;font-weight: bold;">尹君二期 张大爷 近地铁 次卧一朝南 带厕所</view>
			</view>
			<view class="other"><span style="font-size: 10px; color: #808080;margin-left: 10px;">Part·南 | 约 19m2 | 10/19层</span></view>
			<span style="background-color: #50B7EA; font-size: 12px; margin-left:10px;">优惠</span>
			<span style="font-size: 12px;margin-left: 10px;">首月75折</span>
			<view>
				<span style="width:40px; height:25px; line-height:25px; background-color:#e3f6f5;font-size: 12px;margin-left: 5px;">近地铁</span>
				<span style="width:40px; height:25px; line-height:25px; background-color:#e3f6f5;font-size: 12px;margin-left: 5px;">不上夜班</span>
				<span style="width:40px; height:25px; line-height:25px; background-color:#e3f6f5;font-size: 12px;margin-left: 5px;">不带朋友</span>
				<span style="width:40px; height:25px; line-height:25px; background-color:#e3f6f5;font-size: 12px;margin-left: 5px;">不带宠物</span>
			</view>
			<view style="margin-top: 10px; border-top: 1px solid #C8C7CC;">
				<view style="color: #f40; font-size: 14px; font-weight: bold;margin-left: 10px; ">老人约定</view>
				<view style="color: #808080; font-size: 12px;margin-left: 10px; margin-top:10px">不接受上夜班的租客</view>
				<view style="color: #808080; font-size: 12px;margin-left: 10px; margin-top:10px">不接受养宠物的租客</view>
				<view style="color: #808080; font-size: 12px;margin-left: 10px; margin-top:10px">希望20左右的租客</view>
				<view style="color: #808080; font-size: 12px;margin-left: 10px; margin-top:10px">不接受不爱卫生的租客</view>
				<view style="color: #808080; font-size: 12px;margin-left: 10px; margin-top:10px; margin-bottom: 10px;">不接受喜欢带朋友回家的租客</view>
			</view>
			<view style="margin-top: 15px;border-top: 1px solid #C8C7CC;">
				<span
					style="font-weight: bold;font-size: 13px;margin-left: 10px;margin-top: 5px;border-bottom: 1px solid black
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
			<view style="margin-top: 10px;border-top: 1px solid #C8C7CC;">
				<view style="font-size: 14px; font-weight: bold;margin-left: 10px; margin-top: 5px;">小区及周边</view>
			</view>
			<view style="display: flex;margin-left: 10px; margin-top: 10px;">
				<view style="color: blue; border-bottom: 1px solid blue;font-size: 14px;width: 35px;text-align: center;">交通</view>
				<view style="color: #808080; margin-left: 10px;font-size: 14px;">商场</view>
			</view>
			<view><map style="width: 100%; height: 200px;margin-top: 10px;margin-bottom: 10px;" :latitude="latitude" :longitude="longitude" :markers="covers"></map></view>
			<view style="border-top: 1px solid #C8C7CC;">
				<view style="color: #808080;font-size: 14px; margin-top: 10px; margin-bottom: 10px; margin-left: 10px; font-weight: bold;">其他 Part</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return {
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
			}
		}
	}
</script>

<style></style>
