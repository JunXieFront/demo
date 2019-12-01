<template>
	<view >
		<view class="head">请填入你想要提交的相关信息：</view>
		<view class="fir">
			<view class="act">活动名称：</view>
			<input v-model="Detail.title" />
			<view class="act">活动详情：</view>
			<textarea v-model="Detail.details"></textarea>
		</view>
		<view class="sec">
			<view class="act">总活动人数：</view>
			<input v-model="cap" />
		</view>
		<view class="thr">
			<view class="act">剩余需要的人数：</view>
			<input v-model="need" />
		</view>
		<view style="width: 80%;margin: 0 auto;margin-top: 5px;">
			活动时间：
			<view class="four">
				<input class="small" />
				年
				<input class="small" />
				月
				<input class="small" />
				日
			</view>
		</view>
		<button>提交</button>
	</view>
</template>

<script>
export default {
	data() {
		return {
			Detail: {
				title: '',
				details: ''
			},
			house_id: '',
			cap: '',
			joined: '',
			need: '',
			showCaledar: false,
			dateStr: ''
		};
	},
	methods: {},
	components: {}
};
</script>

<style>

.head {
	width: 80%;
	margin: 0 auto;
	padding-top: 15px;
	padding-bottom: 15px;
	color: #555555;
}
.small {
	height: 25px;
	line-height: 25px;
	width: 25%;
}
.four {
	display: flex;
	width: 100%;
	margin: 0 auto;
}
.act {
	height: 25px;
	line-height: 25px;
	width: 80%;
	margin: 0 auto;
}
textarea {
	height: 80px;
	line-height: 20px;
	width: 80%;
	margin: 0 auto;
	padding-left: 10px;
	border-radius: 10px;
	border: 1px solid black;
	padding-top: 5px;
}
input {
	height: 40px;
	width: 80%;
	line-height: 40px;
	margin: 0 auto;
	border: 1px solid black;
	border-radius: 10px;
	padding-left: 10px;
	color: #555555;
}
button {
	height: 40px;
	line-height: 40px;
	width: 85%;
	margin: 0 auto;
	border: 1px solid white;
	border-radius: 15px;
	margin-top: 10px;
}
</style>
