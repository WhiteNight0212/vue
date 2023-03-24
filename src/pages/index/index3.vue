<template>
	<view class="content">
		<view class="rpx">rpx</view>
		<view class="sass">sass</view>
		<view :data-color="color">diy color</view>
		<view v-for="(item, index) in processList" :key="item.id">
			{{ index }}--{{ item.name }}--{{ item.id }}
		</view>
		<view class="vw">vw</view>
		<view v-for="(item ,i ) in filterList">
			{{ item.name }},{{ item.id }}
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			msg: "message",
			color: "bisque",
			list: [
				{ id: 0, name: "🍎" },
				{ id: 1, name: "🍌" },
				{ id: 2, name: "荔枝" },
				{ id: 3, name: "🍇" },
				{ kid: 3, name: "🍇" }
			]
		}
	},
	computed:{
		filterList(){
			return this.list.filter(v=>v.id<=1);
		},
		processList(){
			return this.list.map(v=>{
				v.color = "blue";
				return v;
			});
		}
	}
}
</script>

<style lang="scss">
.rpx {
	width: 750rpx;
	height: 100px;
	background-color: blue;
}

.vw {
	width: 100vw;
	height: 100vh;
	background-color: bisque;
}

.content {
	.sass {
		background-color: red;
	}
}
</style>
