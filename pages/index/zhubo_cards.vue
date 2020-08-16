<template>
	<!-- 主播列表 -->
	<view class="flex flex-wrap">
		<view v-for="(item, i) of data" :key="i" class="zhubo-card">
			<image :src="item.imgUrl" class="rounded zhubo-image" mode="aspectFill"></image>
			<view class="badeg-lt flex rounded-circle align-center px-2">
				<text class="iconfont iconbizhongguanli text-warning"></text>
				<text class="ml-1 text-white font-normal">{{ item.coin }}</text>
			</view>

			<view class="badge-rt flex rounded-circle align-center px-2">
				<text class="text-white font-normal">人气：</text>
				<text class="ml-1 text-white font-normal">{{ item.pv }}</text>
			</view>

			<view class="badge-lb flex rounded-circle align-center px-2"><text class="text-white font-normal">{{ item.title }}</text></view>
			<view class="badge-rb flex rounded-circle align-center px-2">
				<text class="rounded-circle" style="width: 20rpx; height: 20rpx; background-color: red;"></text>
				<text class="ml-1 text-white font-normal">{{ item.state }}</text>
			</view>
		</view>
	</view>
</template>

<script lang="ts">
import Vue from 'vue'
export class ZhuboCard {
	constructor(public imgUrl, public coin, public pv, /* popularity value*/ public title, public state /* 直播中、已结束 */) {}
}

export default Vue.extend({
	props: {
		data: {
			type: Array,
			default: () => []
		}
	},
	data() {
		return {}
	}
})
</script>

<style>
.zhubo-card {
	width: 365rpx;
	height: 365rpx;
	margin: 5rpx;
	position: relative;
}

.zhubo-image {
	width: 100%;
	height: 100%;
}

.badeg-lt {
	background-color: rgba(0, 0, 0, 0.4);
	position: absolute;
	left: 15rpx;
	top: 15rpx;
}

.badge-rt {
	background-color: rgba(0, 0, 0, 0.4);
	position: absolute;
	right: 15rpx;
	top: 15rpx;
}

.badge-lb {
	background-color: rgba(0, 0, 0, 0.4);
	position: absolute;
	left: 15rpx;
	bottom: 15rpx;
}

.badge-rb {
	background-color: rgba(0, 0, 0, 0.4);
	position: absolute;
	right: 15rpx;
	bottom: 15rpx;
}
</style>
