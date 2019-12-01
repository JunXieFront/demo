
<template>
	<view>
		<view class="com_img" v-for="(list,index) in lists" :key="index">
			<view class="top_img"></view>
			<view class="top_txt">{{list.name}}</view>
			<view class="top_phone">{{list.phone}}</view>
		</view>
		<navigator url="person_message/person_message">
			<view class="btn_msg">
				<image src="../../../static/order.png" class="btn_img"></image>
				<view class="msg_txt">我的订单</view>
				<view class="msg_icon"></view>
			</view>
		</navigator>
		<navigator url="history/history">
			<view class="btn_msg">
				<image src="../../../static/room.png" class="btn_img"></image>
				<view class="msg_txt">我的房间</view>
				<view class="msg_icon"></view>
			</view>
		</navigator>
		<navigator >
			<view class="btn_msg">
				<image src="../../../static/party.png" class="btn_img"></image>
				<view class="msg_txt">参与Party</view>
				<view class="msg_icon"></view>
			</view>
		</navigator>
		<navigator>
			<view class="btn_msg">
				<image src="../../../static/about.png" class="btn_img"></image>
				<view class="msg_txt">关于我们</view>
				<view class="msg_icon"></view>
			</view>
		</navigator>
		
		
	
	</view>
</template>

<script>
export default {
	data() {
		return {
			lists:[
				{name:'ADMIN',phone:'13622223333'}
			]
		};
	},
	methods: {}
};
</script>

<style lang="scss">
.com_img {
	height: 40%;
	width: 100%;
}
.top_img {
	height: 80px;
	width: 80px;
	margin: 0 auto;
	background-color: #2c405a;
	border-radius: 50%;
	margin-top: 20px;
}
.top_txt{
	height: 20px;
	width: 100%;
	text-align: center;
	line-height: 20px;
	font-size: 13px;
	margin-top: 9px;
}
.top_phone{
	
	height: 20px;
	width: 100%;
	text-align: center;
	line-height: 20px;
	font-size: 10px;
}
.btn_msg{
	height: 50px;
	width: 80%;
	margin: 0 auto;
	display: flex;
	margin-top: 15px;
	border: 1px solid #2C405A;
	border-radius: 5px;
	line-height: 50px;
}
.btn_img{
	margin-left: 10px;
	height: 20px;
	width: 20px;
	margin-top: 15px;
}

.msg_txt{
	width: 60%;
	height: 100%;
	margin-left: 15px;
}
.msg_icon{
	// background:#007AFF;
	// border: 0;
	height:0;
	width: 0;
	border-top: 10px solid transparent;
	border-bottom:  10px solid transparent;
	border-left: 10px solid #2C405A;
	margin-top: 15px;
}
</style>
