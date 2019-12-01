<template>
	<!-- 全屏 -->
	<view class="all">
		<!-- 分块 -->
		<view class="component" v-for="(list, i) in lists" :key="i">
			<!-- 下单时间 + 情况-->
			<view class="top">
				<span class="time">下单时间：{{ list.time }}</span>
				<span class="case">{{ list.case }}</span>
			</view>
			<!-- 具体情况（图+文） -->
			<view class="detail">
				<image :src="list.src" class="img"></image>
				<!-- 总文字 -->
				<view class="text">
					<!-- 大文字 -->
					<view class="headline">{{ list.headline }}</view>
					<!-- 小文字 -->
					<view class="small_text">
						总额:
						<span class="money">￥{{ list.money }}</span>
						<span class="number">数量：{{ list.number }}</span>
					</view>
				</view>
			</view>
			<view class="bottom">
				<!-- 分类+详情 -->
				<view class="kind">{{ list.kind }}</view>
				<view class="btn">查看详情</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			lists: [
				// { time: '2019-11-21 18:38', case: '已付款', headline: '春熙路*不道伍佰 一元抢购原价998依视路集团蓝光眼镜', money: '10.00', number: '1', kind: '老人' },
				// { time: '2019-11-21 18:38', case: '已付款', headline: '春熙路*不道伍佰 一元抢购原价998依视路集团蓝光眼镜', money: '10.00', number: '1', kind: '老人' },
				// { time: '2019-11-21 18:38', case: '已付款', headline: '春熙路*不道伍佰 一元抢购原价998依视路集团蓝光眼镜', money: '10.00', number: '1', kind: '老人' },
				// { time: '2019-11-21 18:38', case: '已付款', headline: '春熙路*不道伍佰 一元抢购原价998依视路集团蓝光眼镜', money: '10.00', number: '1', kind: '老人' },
				// { time: '2019-11-21 18:38', case: '已付款', headline: '春熙路*不道伍佰 一元抢购原价998依视路集团蓝光眼镜', money: '10.00', number: '1', kind: '老人' }

			]
		};
	},
	methods: {

								// ajsx:	{$.ajax({
								// 			url:'',//地址
								// 			dataType:'json',//数据类型
								// 			type:'post',//类型
								// 			data:data,
								// 			//请求成功
								// 			success:function(data,status){
								// 				alert('成功');
								// 				console.log(data);
								// 				this.$data.lists.time="data.time",
								// 				this.$data.lists.case="data.case",
								// 				this.$data.lists.headline="data.headline",
								// 				this.$data.lists.money="data.money",
								// 				this.$data.lists.number="data.number",
								// 				this.$data.lists.kind="kind"
								// 			},
								// 			//失败/超时
								// 			error:function(XMLHttpRequest,textStatus,errorThrown){
								// 				alert("数据错误");
								// 			},
								// 		})
								// 		return false;

	}
}
</script>

<style>
.all {
	background-color: #f8f8f8;
}
.component {
	height: 170px;
	width: 100%;
	border: 1px solid white;
	background-color: #e3f6f5;
	border-radius: 20px;
	margin-top: 5px;
}
.top {
	height: 30px;
	width: 100%;
	background-color: #bae8e8;
	/* 	border-bottom: 1px solid #999999;
	border-top:  1px solid #999999; */
	display: flex;
}
.time {
	line-height: 30px;
	margin-left: 2px;
	color: #808080;
	font-size: 14px;
	width: 85%;
	margin-left: 5px;
}
.case {
	line-height: 30px;
	font-size: 15px;
	color: #333333;
	width: 15%;
}
.detail {
	height: 110px;
	display: flex;
}
.img {
	height: 100px;
	width: 25%;
	background-color: #bae8e8;
	margin-right: 15px;
	margin-top: 5px;
	margin-left: 5px;
}
.text {
	height: 100px;
	width: auto;
	width: 70%;
	margin-top: 10px;
}
.small_text {
	display: flex;
	font-size: 16px;
}
.headline {
	height: 70px;
	font-size: 16px;
	font-weight: 200;
	margin-right: 10px;
}
.money {
	color: red;
	font-size: 16px;
	margin-left: 2px;
	flex: 3;
}
.number {
	font-size: 16px;
	color: black;
	margin-right: 2px;
	flex: 3;
}
.bottom {
	width: 100%;
	height: 40px;
	display: flex;
	justify-content: space-between;
	line-height: 40px;
}
.kind {
	display: flex;
	width: 60px;
	height: 20px;
	line-height: 20px;
	font-size: 15px;
	border: 10px;
	text-align: center;
	background-color: #9fdfcd;
	cursor: pointer;
	margin-left: 7px;
	color: #2c405a;
	border-radius: 8px;
	display: inline-block;
}
.btn {
	width: 80px;
	height: 20px;
	cursor: pointer;
	border: 1px solid black;
	border-radius: 15px;
	font-size: 14px;
	line-height: 20px;
	text-align: center;
	margin-right: 10px;
	margin-top: px;
}
</style>
