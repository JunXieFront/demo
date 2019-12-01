<template name="listcontainer">

	<view class="list-container">
		<indexlist v-for="item in list" :key="item.id" :price="item.price" :title="item.title" :size="item.size" :side="item.side"
		:floor="item.floor" :transport="item.transport" :labels="item.labels" :imgsrc="item.src"
		/>
	</view>

</template>

<script>
	import indexlist from '../list/list.vue'
	
	export default{
		name:'listcontainer',
		props:['list'],
		onLanch(){
			console.log(this.props.list)
		},
		components:{
			indexlist
		}
	}
</script>

<style>
	.list-container{
		padding:20rpx;
		
	}
	.list-container indexlist{
		margin:20rpx 0;
		display: block;
	}
</style>
